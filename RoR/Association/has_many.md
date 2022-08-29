## has_many Association
- It indicates a one-to-many connection with another model.
- Each instance of the model has zero or more instances of another model.
## Example
[https://guides.rubyonrails.org/images/association_basics/has_many.png]
````ruby
class Author < ApplicationRecord
  has_many :books
end

class Book < ApplicationRecord
  belongs_to :book
end
````
The name of the other model is pluralized when declaring a **has_many** association.
