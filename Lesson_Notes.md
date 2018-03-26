What does inheritence mean?
* We gain all of the properties, and methods, all the built in, it gives us a class with all. 
    Author, will have all the inheritence from the classes. 

   Models need to be capital / Singular. Th table in the db will always be lower-case and plural.   

   How to mke a new model in rails via terminal:

   rails g model Person name age: integer


   What is a migration? It sends the information, and updates the DB. It tells rails to go in, create tables, with the names and specific attrubute we input with the "Rails G person name age: integer"

   The def of migration is ? 


   once we run data mmigrate, we arent ready we ust created the ruby code the bck end that expects a table to beavalible in the db called "people"

   Rails G model Octous name volume:
   If you create this model nd dont want it anymore, you dont hv to manyally go in and delete it, you can delete with "d"

 *Rails d model Octous name volume:(Delete)**


When we run db:migrete, that will take all the migratons that hvent been run, and go ahead and apply everything. 

The migration itself is the link between the rails app and the DB itself!!

Ypu can see the tables fof the libray database it has the model. When you rubn the mig agan, it.

Hey ithin the app its expecting a table, and then the sql fills in the holes to get it.

Rails C loads up all the models we have. To search thru with active record, Person.all;
You can also find 1 specific person with person.find(1)


With Node we had to worry about unfirectiona shu. Ruby is much cleaner code, Find this, 



      * Also after creating something, like a "New.Pers''''''''''''''''''''''''''''''''''''''''''''''""'''''''''''''''




      dont forget to "Save person" with "Person.Save" "Steve.sce;


      This creates a Migration file that looks like this:
```ruby
class CreatePeople < ActiveRecord::Migration[5.0]
  def change
    create_table :people do |t|
      t.string :name
      t.integer :age
      t.string :occupation
    end
  end
end

CREATE TABLE people (
  id INT SERIAL PRIMARY KEY,
  name VARCHAR,
  type INT,
  occupation VARCHAR
);




We should not go in and edit the schema . If we need to make changes, do a new migration. 

Schema.rb is cool it will tell you what the DB side of your rails app code should look like.

Do not mess with the SCHEMA FILE. It will destroy the project. To Alter the schema file, all you do it alter with active record techniques and the update the schema only through Data Migration. 

Pay attention to your ERDs to prevent a lot of headaches in the future. 






Author.all \\{Gets all information about all the Authors}
Author.all.select("name", "Birth_year") \\{Gets the names and birthyears of each author}
Author.all.where('birth_year > 1900') \\{Gets all authors born in the 20th century or later}
Author.create(name: 'Jamie', nationality: 'U.S', birth_year: 2080)  \\{Create a new author with active record}
