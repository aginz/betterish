Controller
1. Static Pages (Home Page) 
   a. #get betterish manifesto
   b. #get meet-our-team
   c. #get contact
2. Posts
3. Comments
4. Users
5. Admin?
6. Categories

Models
1. Posts => title (string), content (text)
   a. has many Posts
   b. belongs to User
   c. has_many_and_belongs_to_many :categories
   d. has_many :categorizations
   e. has_many :categories, through: :categorizations
2. Comment => comment (test), post_id, user_id // name, email (for anonymous users)
   a. belongs to Post
   b. belongs to User
3. User => devise
   a. has many Posts (ADMIN?)
4. Admin
5. Category
   a. has_many_and_belongs_to_many :posts
   b. has_many :categorizations
   c. has_many :categories, through: :categorizations
6. Categorization
   a. belongs_to :posts
   b. belongs_to :category

