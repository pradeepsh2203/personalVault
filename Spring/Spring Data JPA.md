## Types of Entities Relationship
1. One to One (one objects maps to only one object)
2. One to Many (one object can be related to multiple object)
3. Many to One (opp. to One to Many)
4. Many to Many (both sides multiple objects can be related to each other, defined using a join table )

## Types of Mapping
1. Unidirectional (Only one entity knows about the relationship )
2. Bi-Directional (Both the entity knows about the relationship )*preferred*

## Owning Side
The entity that holds the foreign key in the database (The many side of the entity)

## Fetch Types
* Lazy - Data is fetched only when referred.
* Eager - Data is fetched upfront.

JPA 2.1/Hibernate fetch types default
* One to One - Eager
* Many to One - Eager
* One to Many - Lazy
* Many to Many - Lazy

## Cascade Options
Basically it determines how to handle a children entity if a parent entity is removed. By default no cascade options are provided.

## Cool JPA features
* Embeddable types ( You can have complex datatypes )
* Inheritance 
	* Mapped Superclass
	* Single Table
	* Joined Table
	* Table per class
* Update and Create Timestamps :-
	* @PrePersist and @PreUpdate
