## Associations

Sequelize supports the standard associations:
- One-To-One
- One-To-Many 
- Many-To-Many.

 to create them Sequelize provides *four* types of associations

- The HasOne association
- The BelongsTo association
- The HasMany association
- The BelongsToMany association
<br></br>

### *One-To-One relationships*

Let's say we have two models, Foo and Bar. We want to establish a One-To-One relationship between Foo and Bar. We know that in a relational database, this will be done by establishing a foreign key in one of the tables. So in this case, a very relevant question is: in which table do we want this foreign key to be? In other words, do we want Foo to have a barId column, or should Bar have a fooId column instead?

- Implementation

```
Foo.hasOne(Bar);
Bar.belongsTo(Foo);
```
```
EATE TABLE IF NOT EXISTS "foos" (
  /* ... */
);
CREATE TABLE IF NOT EXISTS "bars" (
  /* ... */
  "fooId" INTEGER REFERENCES "foos" ("id") ON DELETE SET NULL ON UPDATE CASCADE
  /* ... */
  ```

### *One-To-Many relationships*

One-To-Many associations are connecting one source with multiple targets, while all these targets are connected only with this single source.

This means that, unlike the One-To-One association, in which we had to choose where the foreign key would be placed, there is only one option in One-To-Many associations. For example, if one Foo has many Bars (and this way each Bar belongs to one Foo), then the only sensible implementation is to have a fooId column in the Bar table. The opposite is impossible, since one Foo has many Bars.

- Implementation




### *Many-To-Many relationships*

Many-To-Many associations connect one source with multiple targets, while all these targets can in turn be connected to other sources beyond the first.

This cannot be represented by adding one foreign key to one of the tables, like the other relationships did. Instead, the concept of a Junction Model is used. This will be an extra model (and extra table in the database) which will have two foreign key columns and will keep track of the associations. The junction table is also sometimes called join table or through table.

- Options

```
Team.hasMany(Player, {
  foreignKey: 'clubId'
});
Player.belongsTo(Team);
```

- Implementation
```
Team.hasMany(Player);
Player.belongsTo(Team);
```



```
const Movie = sequelize.define('Movie', { name: DataTypes.STRING });
const Actor = sequelize.define('Actor', { name: DataTypes.STRING });
Movie.belongsToMany(Actor, { through: 'ActorMovies' });
Actor.belongsToMany(Movie, { through: 'ActorMovies' });
```