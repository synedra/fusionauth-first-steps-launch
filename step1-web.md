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
 <a href='command:katapod.loadPage?[{"step":"intro"}]' 
   class="btn btn-dark navigation-top-left">Back
 </a>
<span class="step-count"> Step 1 of 2</span>
 <a href='command:katapod.loadPage?[{"step":"step2-web"}]' 
    class="btn btn-dark navigation-top-right">Next
  </a>
</div>

<!-- CONTENT -->

## Using the FusionAuth Web UI

This workspace has been jumpstarted with a running fusionauth server and a running application.

In this module you will be working with the web UI.

## Start the FusionAuth Web UI

You may need to wait a few moments while the server comes up. While you wait, try out the auto-run functionality of this tutorial.  When you see a grey block of code with a darker bar to the left of it, click on that grey block to auto-run the command in the terminal to the right.  Try that now.

```
echo "This command shows the auto-run functionality of the tutorial."
```

Now that you've seen how it works, go ahead and run the following command, which will wait until the server is ready for interaction and then start up the administration screen for FusionAuth in a separate window.


```
bash serverup.sh
gp preview `gp url 9011`/admin
```

Login to the Fusionauth UI with the following credentials:

  - Username: admin@example.com
  - Password: password

## Add a New User

In the administration screen, click on the hamburger symbol on the upper left of the screen.  Select "Users"

![Dashboard](/img/dashboard-users-selected.png)

Click the green plus sign in the upper right hand corner to add a new user.

Fill in the user with the information from the image:
- Email: fred@example.com
- Username: fred
- De-select the "Send email to set up password" then set the password to 'password'

![Users](/img/add-user.png)

When you have finished, you'll see the user screen.  


<!-- NAVIGATION -->
<div id="navigation-top" class="navigation-top">
 <a href='command:katapod.loadPage?[{"step":"intro"}]' 
   class="btn btn-dark navigation-top-left">Back
 </a>
<span class="step-count"> Step 1 of 2</span>
 <a href='command:katapod.loadPage?[{"step":"step2-web"}]' 
    class="btn btn-dark navigation-top-right">Next 
  </a>
</div>

