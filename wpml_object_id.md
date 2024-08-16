#WPML Getting Translated Posts with wpml_object_id

The `wpml_object_id` function is quite versatile and can be used with various object types in WordPress to retrieve the ID of the translated version of that object. Here's a list of common object types you can use with `wpml_object_id`:

### 1. **Post Types**
   - **`post`**: For regular posts.
   - **`page`**: For pages.
   - **`custom_post_type`**: For any custom post type registered in WordPress.

### 2. **Taxonomies**
   - **`category`**: For categories.
   - **`post_tag`**: For tags.
   - **`custom_taxonomy`**: For any custom taxonomy registered in WordPress.

### 3. **Menu**
   - **`nav_menu`**: For navigation menus (like in your current use case).

### 4. **Taxonomy Terms**
   - **`term`**: Generic term object type, though usually specific taxonomy names like `category` or `post_tag` are used.
   - **`product_cat`**: For WooCommerce product categories.
   - **`product_tag`**: For WooCommerce product tags.

### 5. **Other WordPress Objects**
   - **`attachment`**: For media attachments.
   - **`user`**: While not directly supported, user-related metadata might be indirectly translated or managed via WPML extensions.

### Example Usages

- **Post Translation**:
  ```php
  $translated_post_id = wpml_object_id( $original_post_id, 'post', true, $current_language );
  ```

- **Custom Post Type Translation**:
  ```php
  $translated_cpt_id = wpml_object_id( $original_cpt_id, 'my_custom_post_type', true, $current_language );
  ```

- **Category Translation**:
  ```php
  $translated_category_id = wpml_object_id( $original_category_id, 'category', true, $current_language );
  ```

- **Menu Translation**:
  ```php
  $translated_menu_id = wpml_object_id( $original_menu_id, 'nav_menu', true, $current_language );
  ```

- **Attachment Translation**:
  ```php
  $translated_attachment_id = wpml_object_id( $original_attachment_id, 'attachment', true, $current_language );
  ```

### Conclusion

The `wpml_object_id` function is a powerful tool when working with WPML, allowing you to retrieve the translated version of various types of WordPress objects, ensuring that your site content adapts correctly based on the language the user is viewing. Whether you're dealing with posts, pages, custom post types, taxonomies, or menus, this function helps keep your site consistent across multiple languages.
