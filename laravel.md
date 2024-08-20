
- [Laravel Routes](#laravel-routes)
  - [Use Kebab-Case for Slugs](#use-kebab-case-for-slugs)
  - [Use Plural Form For Resource Routes](#use-plural-form-for-resource-routes)

## Laravel Routes

### Use Kebab-Case for Slugs

  ❌ Discouraged
  ```php
  Route::get('account_settings', ...);
  Route::get('references/legalBases', ...);
  ```

  ✅ Recommended
  ```php
  Route::get('account-settings', ...);
  Route::get('references/legal-bases', ...);
  ```

  **Reasons to Use Kebab-Case:**
  * **SEO-Friendly:** Search engines parse kebab-case URLs better, boosting SEO.
  * **Readability:** Kebab-case is easier to read than camelCase or snake_case in URLs.
  * **Consistency:** Matches Laravel documentation and common practices, ensuring uniformity.

### Use Plural Form For Resource Routes

  ❌ Discouraged
  ```php
  Route::get('user', ...);
  Route::get('product/category', ...);
  ```

  ✅ Recommended
  ```php
  Route::get('users', ...);
  Route::get('products/categories', ...);
  ```

  **Note:** It's acceptable to use the singular form for non-resource routes, such as:
  ```php
  Route::get('dashboard', ...);
  ```
---