## has_many Association
- It indicates a one-to-many connection with another model.
- Each instance of the model has zero or more instances of another model.
## Example
![This is an image](https://guides.rubyonrails.org/images/association_basics/has_many.png)
![This is an imag](https://guides.rubyonrails.org/images/association_basics/belongs_to.png)
> *has_many* associations must use the pluralized term.

> *belongs_to* associations must use the singular term.
````ruby
class Author < ApplicationRecord
  has_many :books
end

class Book < ApplicationRecord
  belongs_to :author
end
````
