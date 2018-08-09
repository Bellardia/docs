# User Profile Form

If you want to create a form that is able to edit a user’s own profile, you can do so with the following code:

```twig
<form method="post" accept-charset="UTF-8">
    {{ csrfInput() }}
    <input type="hidden" name="action" value="users/save-user">
    {{ redirectInput('users/'~currentUser.username) }}
    <input type="hidden" name="userId" value="{{ currentUser.id }}">
    
    <label for="location">Location</label>
    <input type="text" id="location" name="fields[location]" value="{{ currentUser.location }}">

    <label for="firstName">First Name</label>
    <input type="text" id="firstName" name="firstName" value="{{ currentUser.firstName }}">
    
    <label for="lastName">Last Name</label>
    <input type="text" id="lastName" name="lastName" value="{{ currentUser.lastName }}">
    
    <label for="bio">Bio</label>
    <textarea id="bio" name="fields[bio]">{{ currentUser.bio }}</textarea>

    <input type="submit" value="Save Profile">
</form>
```


Note that custom fields use the fields array in the name attribute, the system *First Name* and *Last Name* fields do not.
