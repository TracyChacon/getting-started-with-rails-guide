# My Rails Tutorial Project

This project is a result of following the official Ruby on Rails Guides tutorial. This repository tracks my progress through the official Ruby on Rails Guides tutorial, covering fundamental Rails concepts. [Click here for a summary of what I learned.](#challeges_learning)

## Technologies Used

- **Ruby:** 3.2.8
- **Ruby on Rails:** 8.0.2
- **Database:** SQLite3 (development/test)
- **Frontend:** HTML, CSS, JavaScript (basic, as per tutorial)

## Setup and Running the Application

To get this project up and running locally, follow these steps:

1.  **Prerequisites:**

    - Ruby (install is operating system dependent see [Ruby Documentation Page](https://www.ruby-lang.org/en/documentation/) )
    - Bundler (`gem install bundler`)

2.  **Clone the Repository:**

    ```bash
    git clone [https://github.com/TracyChacon/getting-started-with-rails-guide.git](https://github.com/TracyChacon/getting-started-with-rails-guide.git)
    cd getting-started-with-rails-guide
    ```

3.  **Install Dependencies:**

    ```bash
    bundle install
    yarn install # if using Rails 7+ with default asset management
    ```

4.  **Database Setup:**

    ```bash
    rails db:migrate

    ```

5.  **Run the Rails Server:**

    ```bash
    rails server
    ```

6.  **Access the Application:**
    Open your web browser and navigate to `http://localhost:3000`.

<h2 id="challeges_learning">Challeges/Learning</h2>

### Overview

This repository documents my structured learning journey through the official Ruby on Rails "Getting Started" guide. I built a simple e-commerce application, named store, to gain practical experience with core Rails concepts, patterns, and development workflows. This project allowed me to solidify my understanding of web application development within the Rails framework, from initial setup to database interaction and routing.

## Challenges and Key Learnings

### Initial Language Barrier: Mastering Ruby Fundamentals

My first significant challenge in this tutorial was immersing myself in the Ruby programming language. While I possess strong foundational knowledge in C, C++, Python, and JavaScript, grasping Ruby's distinct syntax and idiomatic expressions, especially when integrated with Rails, presented a fresh learning curve.

To prepare, I consulted the [official Ruby Documentation](https://www.ruby-lang.org/en/documentation/) and worked through the concise ["Ruby in Twenty Minutes"](https://www.ruby-lang.org/en/documentation/quickstart/) guide to build a foundational understanding of Ruby's core concepts; furthermore, I actively practiced Ruby exercises on [Exercism](https://exercism.org/tracks/ruby), leveraging its interactive approach to reinforce my learning. This proactive approach to understanding Ruby before diving deep into Rails significantly smoothed the learning path for the framework itself.

### Foundational Rails Concepts and Application Development

My journey through the Rails guide provided a comprehensive understanding of the framework's architecture and practical application development.

### Initial guide on getting started with Rails

This section introduces the foundational "Getting Started with Rails" guide,
outlining the key topics covered for new users.

The guide aims to teach:

- Rails installation and application creation.
- Database connection setup for a Rails application.
- The general directory layout of a Rails application.
- Basic principles of MVC (Model, View, Controller) and RESTful design.
- Methods for quickly generating application components.
- How to deploy a Rails app to production using Kamal.

### Lessons Learned in each section

1.  **Introduction to the Rails guide** - This section introduces the initial "Introduction" section for the Ruby on Rails
    guide.

    It sets the stage by:

    - Welcoming new users to Ruby on Rails.
    - Stating that no prior Rails experience is required to follow the guide.
    - Explaining Rails' foundation on the Ruby programming language and
      recommending basic Ruby knowledge for better understanding.
    - Providing links to the official Ruby website and a list of free programming
      books for further learning.

2.  **Outline of Rails philosophy and guiding principles** - This is a section detailing the core philosophy and guiding
    principles behind the Rails framework.

    This section covers:

    - **Introduction to Rails:** Briefly describes Rails as a Ruby web application
      framework designed for ease of development and increased productivity.
    - **Opinionated Software:** Explains that Rails is opinionated, promoting a
      "best" way of doing things, which leads to higher productivity when
      following "The Rails Way."
    - **Guiding Principles:** Highlights two major principles:
      - **Don't Repeat Yourself (DRY):** Emphasizes the importance of
        single, unambiguous representation of knowledge to improve
        maintainability, extensibility, and reduce bugs.
      - **Convention Over Configuration:** Describes how Rails leverages
        sensible defaults and conventions, minimizing the need for
        extensive configuration.

3.  **Initialize new Rails application and introduce core concepts** - This section is about setting up the foundational `store` e-commerce application, outlining the prerequisites, creation process, directory structure, and the core
    Model-View-Controller (MVC) architecture of Rails.

    This section covers:

    - **Prerequisites Check:** Instructions to verify Ruby (3.2+) and Rails (8.0.0+)
      versions, ensuring the development environment is ready.
    - **Application Generation:** Demonstrates creating a new Rails application
      named `store` using `rails new store`, along with options for customization.
    - **Directory Structure Overview:** Provides a comprehensive breakdown of the
      files and directories generated by `rails new`, explaining the purpose of
      key folders like `app/`, `bin/`, `config/`, `db/`, `Gemfile`, `log/`,
      `public/`, `test/`, and others.
    - **MVC Basics:** Introduces the fundamental Model-View-Controller architecture
      of Rails, defining the roles of:
      - **Model:** Manages application data (e.g., database tables).
      - **View:** Handles rendering responses (e.g., HTML, JSON).
      - **Controller:** Manages user interactions and request logic.

4.  **Initial Rails server setup and verification** - My first interaction with the Rails application by
    booting up the Rails server and verifying its functionality.

    This section covers:

    - Instructions for starting the Rails server using `bin/rails server`.
    - Explanation of why `bin/rails` should be used for commands within the
      application directory.
    - Details about the Puma web server and its output upon startup,
      including listening addresses (`http://localhost:3000`).
    - Guidance on accessing the default Rails welcome page in the browser as
      a "smoke test" to confirm successful setup.
    - Instructions for stopping the server using `Ctrl-C`.
    - Explanation of Rails' automatic code reloading feature in development,
      highlighting how it enhances developer experience by eliminating the
      need for server restarts after code changes.
    - Brief mention of Rails' naming conventions for automatic file loading,
      reducing the need for explicit `require` statements.

5.  **Creating a Database Model** - I learned about the foundational `Product` model for the e-commerce
    store, enabling the creation and management of product data in the database:
    This section covers:

    - Generating a `Product` model with a `name:string` attribute using
      `bin/rails generate model Product name:string`.
    - Explaining the purpose of **Active Record** in mapping relational databases
      to Ruby code and its role in generating SQL.
    - Detailing the artifacts created by the model generation command: a database
      migration, the `Product` Active Record model, and associated tests/fixtures.
    - Clarifying **database migrations** as a mechanism for tracking and applying
      database schema changes, ensuring consistency between development and
      production environments.
    - Providing a deep dive into the generated migration file
      (`db/migrate/<timestamp>_create_products.rb`), explaining:
      - The `create_table :products` block and the convention of plural table
        names.
      - The `t.string :name` column definition.
      - The `t.timestamps` shortcut for `created_at` and `updated_at` columns.
    - Demonstrating how to apply the migration to the database using
      `bin/rails db:migrate` and explaining its output.
    - Briefly mentioning `bin/rails db:rollback` for undoing migrations.

6.  **How to use the Rails console** - Shows how to interact with the application, specifically after creating the products table.
    This section covers:

    - Explaining the purpose and utility of the Rails console as an interactive
      testing tool.
    - Instructions on how to access the console via `bin/rails console`.
    - A practical example of using `Rails.version` to verify console functionality.

7.  **Acitive Record Model Basics** - This forms a critical part of a Rails application, enabling robust data management and interaction with the backend database and estblished the foundational knowledge of Rails Active Record models, which serve as the object-relational mapping (ORM) layer for interacting with the database. Key takeaways include:

    - **Model Definition:** Understanding that `app/models/product.rb` (e.g., `class Product < ApplicationRecord; end`) defines a model, and Rails automatically infers database columns and types.
    - **Dynamic Attribute Generation:** How Rails queries the database (e.g., `Product.column_names`) to dynamically generate attributes for model instances, eliminating boilerplate code.
    - **Creating Records:**
      - **`Product.new`:** Instantiating a new model instance in memory.
      - **`#save`:** Persisting an in-memory instance to the database, triggering an `INSERT` SQL query and populating `id`, `created_at`, and `updated_at` timestamps.
      - **`Product.create`:** A convenient class method to instantiate and save a record in a single step.
    - **Querying Records:**
      - **`Product.all`:** Retrieving all records from the corresponding database table, returning an `ActiveRecord::Relation` object.
      - **`Product.where`:** Filtering records based on specific column values, also returning an `ActiveRecord::Relation`.
      - **`Product.order`:** Sorting query results (e.g., `name: :asc`).
      - **`Product.find(id)`:** Retrieving a single record by its primary key (`id`).
    - **Updating Records:**
      - **`#update`:** Updating attributes and saving changes to the database in one go, triggering an `UPDATE` SQL query.
      - **Assigning attributes and `#save`:** Manually assigning attribute values to an instance and then calling `#save` to persist changes.
    - **Deleting Records:**
      - **`#destroy`:** Deleting a specific record from the database, triggering a `DELETE` SQL query.
    - **Validations:**
      - Implementing data integrity rules (e.g., `validates :name, presence: true`) in the model.
      - Understanding how Rails automatically runs validations on `create`, `update`, and `save` operations.
      - Accessing validation errors via `#errors` and `#errors.full_messages` for user feedback.

8.  **Requests** - Core Rails request-response flow explanation that establishes the basic "request's journey" through a Rails application and gives overview of **routes**, **controllers (with actions)**, and **views**.
    This section covers:

    - **Routes:** Map incoming HTTP requests to specific controller actions.
    - **Controllers:** Ruby classes containing "actions" (public methods) that handle the request logic and prepare data.
    - **Views:** Templates (typically HTML and Ruby) responsible for presenting data in a desired format to the user.

9.  **Routes**
    This section lays the groundwork for building interactive web applications by establishing how user requests are received and processed within the Rails framework.

    This section covers:

    - **Anatomy of a URL:** Understanding protocol, host, path, and query parameters.
    - **HTTP Methods:** Differentiating between GET, POST, PUT, PATCH, and DELETE requests and their purposes.
    - **Rails Routes:** How `config/routes.rb` maps HTTP methods and URL paths to controller actions (e.g., `get "/products", to: "products#index"`).
    - **Route Parameters:** Utilizing dynamic segments in URLs (e.g., `:id`, `:title`) to capture data for controller use.
    - **CRUD Routes:** The eight common routes for Create, Read, Update, and Delete operations on a resource (index, new, create, show, edit, update, destroy).
    - **Resource Routes:** The `resources :products` shortcut for automatically generating all standard CRUD routes for a given resource, significantly reducing boilerplate.
    - **`bin/rails routes` command:** Using this command to inspect and verify all defined routes in the application, including those generated by `resources`.

10. **Controllers & Actions** - This section introduces the full CRUD (Create, Read, Update, Delete) functionality for Products, leveraging Rails' conventions for controllers, views, and helpers.

    This section covers:

    - **ProductsController:**

      - Generated `ProductsController` with `index` action (`bin/rails generate controller Products index --skip-routes`).
      - Implemented `index` action to display all products (`@products = Product.all`).
      - Implemented `show` action to display individual products (`@product = Product.find(params[:id])`).
      - Implemented `new` and `create` actions for product creation, including `product_params` for strong parameters and error handling with `render :new, status: :unprocessable_entity`.
      - Implemented `edit` and `update` actions for product modification, similarly handling strong parameters and errors.
      - Implemented `destroy` action for product deletion.
      - Utilized `before_action :set_product, only: %i[show edit update destroy]` to DRY up product fetching logic.

    - **Views:**

      - Created `app/views/products/index.html.erb` to list products with links to show/new.
      - Created `app/views/products/show.html.erb` to display individual product details with links to edit/back.
      - Created `app/views/products/new.html.erb` for the new product form.
      - Created `app/views/products/edit.html.erb` for the edit product form.
      - Extracted the product form into a `_form.html.erb` partial for reuse in new and edit views.
      - Used ERB tags (`<%= %>` for output, `<% %>` for execution) and Rails helpers (`link_to`, `form_with`, `button_to`, `debug`).

    - **Routing:**

      - Set `root "products#index"` in `config/routes.rb` to make `/` display the product index.

    - **User Experience:**
      - Incorporated `data-disable-with` on submit buttons for better UX during form submission.
      - Added `data-turbo-confirm` for delete operations.

11. **Basic user authentication** - This section introduces a basic authentication system to secure product management, leveraging Rails' built-in authentication generator.

    Key ideas include:

    - Generated authentication boilerplate (`bin/rails generate authentication`) for `User` and `Session` models, along with their respective controllers and views.
    - Migrated the database to create `users` and `sessions` tables (`bin/rails db:migrate`).
    - Ensured `bcrypt` gem is included and functional for secure password hashing.
    - Implemented a "Log out" button in the application layout, visible only when authenticated.
    - Configured `ProductsController` to allow unauthenticated access to `index` and `show` actions (`allow_unauthenticated_access only: %i[index show]`).
    - Dynamically displayed "New product," "Edit," and "Delete" links in product views only for authenticated users, enhancing security and user experience.

12. Caching Products - Implement product header caching for performance improvement. This section introduces caching for the product header in `app/views/products/show.html.erb` to improve page load performance.

    - Leverages Rails' **Solid Cache** to store HTML fragments.
    - Utilizes the **`cache` helper with `@product`** to generate unique, dynamic cache keys. This ensures efficient caching and automatic invalidation of the cache when product records are updated, preventing stale data.
    - **Enables caching in development** by running `bin/rails dev:cache`, allowing developers to observe caching behavior.
    - **Provides clear log visibility**, showing "Read fragment" for cache hits and "Write fragment" for initial cache generation, aiding in debugging and monitoring.

13. Rich Text Fields with Action Text - Implement rich text description for products using Action Text

    This section introduces rich text capabilities for product descriptions using Rails Action Text. Users can now add and display rich text content, including formatting, for product descriptions.

    This section covers:

    - **Installation of Action Text:** Ran `bin/rails action_text:install`, `bundle install`, and `bin/rails db:migrate`.
    - **Product Model Update:** Added `has_rich_text :description` to the `Product` model.
    - **Form Integration:** Updated `app/views/products/_form.html.erb` to include `form.rich_text_area :description`.
    - **Controller Strong Parameters:** Modified `products_controller.rb` to permit the `:description` parameter.
    - **Show View Display:** Updated `app/views/products/show.html.erb` to render `@product.description`.

14. File Uploads with Active Storage - Implement direct file uploads for product featured images with Active Storage

    This section enhances product management by integrating Active Storage for direct file uploads, specifically for a featured image.

    This builds upon the existing Active Text functionality, allowing for a dedicated featured image per product.

    Users can now upload and display a dedicated featured image for each product, alongside the existing rich text capabilities.

    Key changes include:

    - **Product Model Update:** Added `has_one_attached :featured_image` to the `Product` model.
    - **Form Integration:** Updated `app/views/products/_form.html.erb` to include a file upload field for `:featured_image`.
    - **Controller Strong Parameters:** Modified `products_controller.rb` to permit the `:featured_image` parameter.
    - **Show View Display:** Added logic to `app/views/products/show.html.erb` to display the featured image if attached.

## Credits and Acknowledgements

This project is based on and follows the official [Ruby on Rails Guides: Getting Started with Rails](https://guides.rubyonrails.org/getting_started.html) tutorial.

## License

This work is licensed under a Creative Commons Attribution-ShareAlike 4.0 International License.
For the full license text, see [LICENSE @ https://creativecommons.org/licenses/by-sa/4.0/](https://creativecommons.org/licenses/by-sa/4.0/).
