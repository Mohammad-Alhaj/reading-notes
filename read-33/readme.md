# Reading: Login  and  Auth 


**DEFINITION OF ROLE-BASED ACCESS CONTROL (RBAC)**
Role-based access control (RBAC) restricts network access based on a person's role within an organization and has become one of the main methods for advanced access control. The roles in RBAC refer to the levels of access that employees have to the network.

Employees are only allowed to access the information necessary to effectively perform their job duties. Access can be based on several factors, such as authority, responsibility, and job competency. In addition, access to computer resources can be limited to specific tasks such as the ability to view, create, or modify a file.

As a result, lower-level employees usually do not have access to sensitive data if they do not need it to fulfill their responsibilities. This is especially helpful if you have many employees and use third-parties and contractors that make it difficult to closely monitor network access. Using RBAC will help in securing your company’s sensitive data and important applications.


**some an example of RBAC including**
Through RBAC, you can control what end-users can do at both broad and granular levels. You can designate whether the user is an administrator, a specialist user, or an end-user, and align roles and access permissions with your employees’ positions in the organization. Permissions are allocated only with enough access as needed for employees to do their jobs.

What if an end-user's job changes? You may need to manually assign their role to another user, or you can also assign roles to a role group or use a role assignment policy to add or remove members of a role group.

**BENEFITS OF RBAC**

1-Reducing administrative work and IT support.

2-Maximizing operational efficiency. 

3-Improving compliance


## react-cookie

Getting started
npm install react-cookie

or in the browser (global variable ReactCookie):
``` javascript
<script
  crossorigin
  src="https://unpkg.com/react@16/umd/react.production.js"
></script>
<script
  crossorigin
  src="https://unpkg.com/universal-cookie@3/umd/universalCookie.min.js"
></script>
<script
  crossorigin
  src="https://unpkg.com/react-cookie@3/umd/reactCookie.min.js"
></script>
```

useCookies([dependencies])
Access and modify cookies using React hooks.

const [cookies, setCookie, removeCookie] = useCookies(['cookie-name']);
React hooks are available starting from React 16.8

dependencies (optional)
Let you optionally specify a list of cookie names your component depend on or that should trigger a re-render. If unspecified, it will render on every cookie change.

cookies
Javascript object with all your cookies. The key is the cookie name.
