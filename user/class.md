# User Class Variables, Functions, and Methods

## Variables

-  **$cms->user->role `(string)` ** The current user role
-  **$cms->user->permissions `(array)` ** All permissions granted to current user
-  **$cms->user->id `(integer)` ** User's id if logged in, false if not logged in
-  For users that are logged in:
   -  **$cms->user->first `(string)` ** User's first name
   -  **$cms->user->last `(string)` ** User's last name
   -  **$cms->user->name `(string)` ** User's publicly visible name (defaults to first + last name)
   -  **$cms->user->email `(string)` ** User's email address
   -  **$cms->user->phone `(string)` ** User's phone number
   -  **$cms->user->meta `(object)` ** User's meta data

## Functions

-  **$cms->user->can(`$permission`) `(boolean)` ** Returns `true` if user is granted `$permission`.
-  For users with `edit_users` permission:
   -  **$cms->user->create(`$email`, `$data`)** Creates a new user. `$email` is required. Returns user id if successful.
      -  `$data` associative array or object with the following _option_ parameters:
         -  `first` User's first name
         -  `last` User's last name
         -  `name` User's publicly visible name (defaults to first + last name)
         -  `phone` User's phone number
         -  `roles` User's role. If omitted, `registered` will be the default role.
         -  `permissions` Associative array or object with an `include` and `exclude` parameter. Use this exclusively to override granted/excluded permissions in the user's role.
            -  `include` Array of permissions granted
            -  `exclude` Array of permissions excluded
         -  `meta` Associative array or object with custom meta data for the user in key / value pairs
   -  **$cms->user->delete(`$id`)** Deletes a specific user. The current user must have `edit_users` permission for this to work. Returns `true` if successful.

## Methods

-  **$cms->user->logout()** Ends the current user's session.
