This application that I've forked from Alex Wolf repository is just great!
All I needed to do was a litte change in the configuration so as to make it use the app configuration to store and read the API key and the Endpoint, things that must be private!
According to this, the Application.config file should be kind of:



This is the origital Readme that Alex wrote originally:

## Chat with your SQL Data

This is the demo app for the youtube video: https://www.youtube.com/watch?v=hw6oTjw9_Ro

The app uses AI to generate queries for a relational SQL database based on natural language, meaning there is no requirement for an indexing search service, vector queries, or other usual AI architectures.

The AI service does NOT index any of your data, it just needs the basic table schema to understand how your database is structured. It generates queries based on these relationships.

Important: This app works best with small to medium sized databases with clear table relationships based on standard primary key and foreign key relationships with clear naming.

There is no troubleshooting support provided, feel free to fork the app and use for your own purposes.

## Setup steps

1. In the `SchemaLoader` project, replace the connection string placeholder with your own database connection, then run the app to generate your schema. Copy the schema into a text file for later use.

2. In the `YourOwnData` project, in the DataService.cs file, replace the connection string placeholder with your own database connection - the same connection string as in step 1.

3. In the `Index.cshtml.cs` file, replace the YOUR_SCHEMA placeholder in the AI prompt instructions section with the schema you copied previously.

4. In the `Index.cshtml.cs` file again, replace the OpenAI placeholder values towards the top so the app can connect to your AI service.
