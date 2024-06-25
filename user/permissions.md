# Permissions

Each role can define a set of default permisions, these permissions are assigned to the user when assigned the role in the CMS. There are two properties for defined in the json for each role, `include` and `exclude`.

The `include` propert sets the initial set of permissions allowed for the user. The `exclude` property is used to exclude specific posts or types from the properties defined in include.

A good use case for the `exclude` property could be; giving a visitor permissions for `view_posts`, but having `view_posts_locked` in the exclude property. `locked` would be a post type that is only visible when logged in, so while it is excluded in the `guest` role, you would not exclude it in the `registered` role.

## Permissions List

-  **publish_code:** User can publish code assets from staging to production
-  **publish_posts:** User can publish all post types
-  **publish_posts\_`type`:** User can publish specific post type
-  **publish_posts\_`id`:** User can publish specific post id
-  **publish_collections:** User can publish all collection types
-  **publish_collections\_`type`:** User can publish specific collection type
-  **publish_options:** User can publish all options pages
-  **publish_options\_`id`:** User can publish specific options page
-  **publish_parts:** User can publish all parts
-  **publish_parts\_`type`:** User can publish specific part type
-  **edit_posts:** User can edit all post types
-  **edit_posts\_`type`:** User can edit specific post type
-  **edit_posts\_`id`:** User can edit specific post id
-  **edit_collections:** User can edit all collection types
-  **edit_collections\_`type`:** User can edit specific collection type
-  **edit_options:** User can edit all options pages
-  **edit_options\_`id`:** User can edit specific options page
-  **edit_parts:** User can edit all parts
-  **edit_parts\_`type`:** User can edit specific part type
-  **edit_users:** User can edit all users
-  **view_posts:** User can view all post types
-  **view_posts\_`type`:** User can view specific post type
-  **view_posts\_`id`:** User can view specific post id
-  **view_collections:** User can view all collection types
-  **view_collections\_`type`:** User can view specific collection type
-  **view_parts:** User can view all parts
-  **view_parts\_`type`:** User can view specific part type
-  **view_archives:** User can view all archives
-  **view_archives\_`type`:** User can view archives for specific post type
-  **view_sections:** User can view all sections
-  **view_sections\_`type`:** User can view specific section types
