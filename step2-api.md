<!-- TOP -->
<div class="top">
  <img src="https://cdn.prod.website-files.com/617b1b1f42c1da41aeae3413/6573599a9ea8c6ccef655afd_primary-logo.png" width=200/>
  <div class="scenario-title-section">
    <span class="scenario-title"><h3>Adding a New User</h3></span>
    <br />
    <span class="scenario-subtitle">ℹ️ For feedback, please contact us via <a href="mailto:kirsten.hunter@fusionauth.io">email</a>.</span>
  </div>
</div>

<!-- NAVIGATION -->
<div id="navigation-top" class="navigation-top">
 <a href='command:katapod.loadPage?[{"step":"step1-api"}]' 
   class="btn btn-dark navigation-top-left">Back
 </a>
<span class="step-count"> Step 2 of 2</span>
 <a href='command:katapod.loadPage?[{"step":"finish"}]' 
    class="btn btn-dark navigation-top-right">Next
  </a>
</div>

<!-- CONTENT -->

## Registering the User with an Application

In this step, you will add the user to an application in the system.  You will be using the "ChangeBank" and once the user is added you'll log into the system with that user to see how that works.

### Search for the Application

First, you need to find information about the application.  To do this, use the following command (again, click in the grey area to run it in the terminal).  The application created from the kickstart is called "ChangeBank" so the first step is to search for that application here:

```
http :9011/api/application/search name=="ChangeBank" | jq .applications[].id
```

Now, we'll register the user with that application:

```
http POST :9011/api/user/registration user:='{"email":"fred@example.com","password":"password"}' registration:='{"applicationId":"e9fdb985-9173-4e01-9d73-ac2d60d1dc8e"}' -vvv
```

## Login to the Application with the User

Now that you've added the user to the application, you can login to the application with that user.

First, launch a browser pointed to ChangeBank:

```
gp preview `gp url 3000`
```

Next, login using fred@example.com with password 'password' to verify that the user was added.

<!-- NAVIGATION -->
<div id="navigation-top" class="navigation-top">
 <a href='command:katapod.loadPage?[{"step":"step1-api"}]' 
   class="btn btn-dark navigation-top-left">Back
 </a>
<span class="step-count"> Step 2 of 2</span>
 <a href='command:katapod.loadPage?[{"step":"finish"}]' 
    class="btn btn-dark navigation-top-right">Next 
  </a>
</div>

