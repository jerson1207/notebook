# The has_and_belongs_to_many Association
A has_and_belongs_to_many association creates a direct many-to-many connection with another model, with no intervening model. This association indicates that each instance of the declaring model refers to zero or more instances of another model. For example, if your application includes assemblies and parts, with each assembly having many parts and each part appearing in many assemblies, you could declare the models this way:
````ruby
class Assembly < ApplicationRecord
  has_and_belongs_to_many :parts
end

class Part < ApplicationRecord
  has_and_belongs_to_many :assemblies
end
````
![This is an image](https://guides.rubyonrails.org/images/association_basics/habtm.png)

### Drawbacks
- it does not have model.
  - you can not create validation
