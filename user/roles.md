# User Roles

Edit roles can be done in _/cms/config/roles.json_.

The "visitor" role is the default role given to anonymous visitors to your website.

The "registered" role is the default role given to users registered through the cms_user_register() function;

The "admin" role is set by default giving full access to all features.

## Default Config

```json
{
   "guest": {
      "include": [
         "view_parts",
         "view_posts",
         "view_archives",
         "view_collections",
         "view_sections"
      ],
      "exclude": []
   },
   "registered": {
      "include": [
         "view_parts",
         "view_posts",
         "view_archives",
         "view_collections",
         "view_sections",
         "edit_user_[[user_id]]"
      ],
      "exclude": []
   },
   "admin": {
      "label": "Admin",
      "include": [
         "publish_code",
         "publish_posts",
         "publish_collections",
         "publish_options",
         "publish_parts",
         "edit_posts",
         "edit_collections",
         "edit_options",
         "edit_parts",
         "edit_users",
         "view_parts",
         "view_posts",
         "view_archives",
         "view_collections",
         "view_sections"
      ],
      "exclude": []
   }
}
```

## Variables

-  **$cms->user->role:** The current user role
-  **$cms->user->permissions:**

## Functions

-  **$cms->user->can('`permission`'):** Returns `true` if user is granted the specified permission
