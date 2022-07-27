# Spring Framework



#### Spring batch

- Spring batch is one of the core module of spring framework and using this spring batch you can create robust batch processing system.

- Batch processing is a technique which processes data in a large group instead of a single element of data where you can process a high volume of data with minimal human interaction.

##### When to use 
Whenever you want to transform huge number of data from source to destination then that time you can make use of spring batch concept.

For Eg: If I have a large data set in csv file that i need to move into db, writing insert query will be a tedious job. Or we want to generate report everyday from db then we can make use of batch.

##### Spring batch core components

###### Job Launcher 
- It is an interface
- It is used to launch a spring boot job
- It is an entry point to initiate a spring batch job 
- It has method run() that will trigger the Job object
- Once the Job Job object called it will also call the Job Repository to maintain the status of Job wether it is fail or success.
- Job will call Step and Step has following three components
	- ItemReader : It will read the data from source
	- ItemProcessor : It will process the data and handle all other operation
	- ItemWriter : ItemWriter will help us to write the data to destination
	
	> Job can have multiple steps and Steps can have ItemReader, ItemProcessor, ItemWriter

	