# My Rails Tutorial Project

This project is a result of following the official Ruby on Rails Guides tutorial. This repository tracks my progress through the official Ruby on Rails Guides tutorial, covering fundamental Rails concepts.

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

## Credits and Acknowledgements

This project is based on and follows the official [Ruby on Rails Guides: Getting Started with Rails](https://guides.rubyonrails.org/getting_started.html) tutorial.

## License

This work is licensed under a Creative Commons Attribution-ShareAlike 4.0 International License.
For the full license text, see [LICENSE @ https://creativecommons.org/licenses/by-sa/4.0/](https://creativecommons.org/licenses/by-sa/4.0/).
