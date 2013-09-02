## Experiments in data mining, entity disambiguation and how to think data-structures for designing beautiful algorithms
### Ekta Grover 

#### Thinking about the Data Mining problem
* What is data? How to represent it?
* Interesting relationships?
* Define your objective function.
* How to know tht score represents the direction you want to capture ?
* How to measure the performance?

#### Problem #1: Entity Disambiguation
* Entity disambiguation is not deterministic
* From Reid Hoffman's book: How much is your network really worth?
* What is information?
	* Information = Related + Unrelated
	* Extract significant attributes/features
	* Relationships between entities and features
* Approach:
	* Preprocessing: Lower case conversion and remove punctuation
	* Exploratory analysis: Create frequency plots
	* Tokenization
	* Handling stop words and i18n
	* Frequent item-set mining with support = # of baskets
	* Post processing, frequency plots and visualization
	* Find number of significant words in an entity name?
	* ??
* [github.com/ekta1007/Experiments-in-Data-Mining](github.com/ekta1007/Experiments-in-Data-Mining) (

* Limitations of this approach
	* Abbreviations
	* Differently referenced entities
	* Sub-entities
	* Inadvertent typos

Note: Goddamnit! My laptop's battery has drained out. Can someone please send a pull request with rest of the notes?