# My Rails Tutorial Project

This project is a result of following the official Ruby on Rails Guides tutorial. This repository tracks my progress through the official Ruby on Rails Guides tutorial, covering fundamental Rails concepts.

The [Getting Started with Rails Tutorial](https://guides.rubyonrails.org/getting_started.html) has the below learning objectives:

- How to install Rails, create a new Rails application, and connect your application to a database.

- The general layout of a Rails application.

- The basic principles of MVC (Model, View, Controller) and RESTful design.

- How to quickly generate the starting pieces of a Rails application.

- How to deploy your app to production using Kamal.

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

## Challeges/Learning

My first challenge embarking on this Rails tutorial was the Ruby language itself. While I have prior experience with C, C++, Python, and JavaScript, understanding Ruby's syntax and idiomatic expressions presented a new hurdle, especially when coupled with the intricacies of Rails.

To address this, I undertook several preparatory steps. I extensively consulted the [official Ruby Documentation](https://www.ruby-lang.org/en/documentation/) to grasp core concepts and worked through the ["Ruby in Twenty Minutes"](https://www.ruby-lang.org/en/documentation/quickstart/) guide to gain a foundational understanding. Additionally, I joined [Exercism](https://exercism.org/tracks/ruby) and began practicing Ruby exercises. This platform appealed to me as a fun and effective way to reinforce my learning; I had already explored it prior to a community recommendation. While "The Odin Project" was also suggested, I ultimately chose Exercism due to my prior familiarity and its interactive learning approach.

7. Acitive Record Model Basics

This forms a critical part of a Rails application, enabling robust data management and interaction with the backend database and estblished the foundational knowledge of Rails Active Record models, which serve as the object-relational mapping (ORM) layer for interacting with the database. Key takeaways include:

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

8. Core Rails request-response flow explanation that establishes the basic "request's journey" through a Rails applicationi and gives overview of **routes**, **controllers (with actions)**, and **views**.

- **Routes:** Map incoming HTTP requests to specific controller actions.
- **Controllers:** Ruby classes containing "actions" (public methods) that handle the request logic and prepare data.
- **Views:** Templates (typically HTML and Ruby) responsible for presenting data in a desired format to the user.

9. Routes
   This section lays the groundwork for building interactive web applications by establishing how user requests are received and processed within the Rails framework.

Summary:

- **Anatomy of a URL:** Understanding protocol, host, path, and query parameters.
- **HTTP Methods:** Differentiating between GET, POST, PUT, PATCH, and DELETE requests and their purposes.
- **Rails Routes:** How `config/routes.rb` maps HTTP methods and URL paths to controller actions (e.g., `get "/products", to: "products#index"`).
- **Route Parameters:** Utilizing dynamic segments in URLs (e.g., `:id`, `:title`) to capture data for controller use.
- **CRUD Routes:** The eight common routes for Create, Read, Update, and Delete operations on a resource (index, new, create, show, edit, update, destroy).
- **Resource Routes:** The `resources :products` shortcut for automatically generating all standard CRUD routes for a given resource, significantly reducing boilerplate.
- **`bin/rails routes` command:** Using this command to inspect and verify all defined routes in the application, including those generated by `resources`.

## Credits and Acknowledgements

This project is based on and follows the official [Ruby on Rails Guides: Getting Started with Rails](https://guides.rubyonrails.org/getting_started.html) tutorial.

## License

This work is licensed under a Creative Commons Attribution-ShareAlike 4.0 International License.
For the full license text, see [LICENSE @ https://creativecommons.org/licenses/by-sa/4.0/](https://creativecommons.org/licenses/by-sa/4.0/).
