# ListTracker-SD4x-React-Homework
This is my code for the "List Tracker" homework from UPenn's Programming for the Web with Javascript.

Specifications (adapted from the SD4x platform on EdX):

Homework 5 - React

In this assignment, you will develop a simple application to track lists of items using React.

The application you will be building has many components that work together in order to organize multiple lists. Such an app could theoretically be used to create a shopping list, a set of daily tasks, or so forth.

In completing this assignment, you will:

- Gain experience understanding and modifying an existing React app

- Use the Node framework to create and deploy a React app with multiple components defined in separate files

- Gain more experience in implementing callback functions in React components that affect the components’ appearance

- Apply what you have learned in the lessons about the relationships between React components and how components interact


Getting Started

To complete this assignment, you will need to set up a development environment that uses Node.js and the create-react-app package using the steps below; you will likely need sudo/root access for each of these steps:

Install Node.js locally by downloading it from https://nodejs.org/en/download/

From the Terminal, Command Prompt, etc. update Node Package Manager by typing the command: npm install npm –g

Install the create-react-app package by typing the command: npm install –g create-react-app

Create a new folder or directory for your project, then navigate to it using Terminal, Command Prompt, etc.

Create the project by typing the command: create-react-app lists

This will create a “lists” directory and install the default React app there. You can start it by changing to the “lists” directory and typing the command: npm start

You should then be able to access http://localhost:3000 using your web browser and see the default React app. If so, you’re ready to proceed.

Start by downloading React-lists.zip. This contains the files you need in order to start building this app.

To install the app:

Extract the files from the .zip file that you downloaded

Copy index.html into the “public/” directory of your React project; this will overwrite the default index.html that is already there.

Copy the seven .js files and App.css into the “src/” directory of your React project; this will overwrite the default index.js, App.js and App.css that are already there.

Activity

The goal of this assignment is to modify the code we have provided so that the user can:

- Create a new list

- Add items to that list

- Mark items by changing their color


The App component is the main component of the app and its render function creates two additional components:

- AddList, which is responsible for taking user input and passing information back to the App component in order to create a new list

- Lists, which is empty when the App is first rendered, but contains all instances of individual List components, each of which contains an AddItem component for adding items and ListItem components for all items in the list

Each component is implemented in a separate file, which has the same name as the component.

Before proceeding, be sure you understand the role of each component in the app and how the components are related.


Part 1. Creating a new List

In the image above, we see the App component render two child components: AddList and Lists. The AddList component contains the text input field next to the words “What will be on your next list?” and a button labeled “Create List”. The Lists component by default reads “Add new lists to get started!”, but will eventually display each individual List component, which consists of an AddItem component and ListItem components.

Implement the AddList.handleSubmit and App.handleAddList functions and modify the components as necessary so that it is possible for the user to create a new list and see the List and AddItem components rendered in the page. In particular, the app should behave as follows:

When the user types the name of a new list into the input field of the AddList component and clicks the “Create List” button, the AddList component should call the AddList.handleSubmit function, which should then update its state and then use the App.handleAddList function to update the state of the App (specifically, the “lists” and “items” variables in the state, as described in the code comments and according to the example below).

The App should then re-render, and with the App’s state now containing a new list, the App should pass the necessary information from its state to the Lists component, which will render a new List component representing a single list.


Part 2. Adding ListItems to a List

Now implement the AddItem.handleSubmit and App.handleAddItem functions and modify the components as necessary so that it is possible for the user to use the AddItem component to add an item to a list and see the ListItem component rendered in the page. In particular, the app should behave as follows:

When the user enters a value in the input field of the AddItem component and clicks the “Submit” button, the AddItem component should call the AddItem.handleSubmit function, which should update the component’s state and then use the App.handleAddItem function to update the state of the App (specifically, the “items” variable in the state, as described in the code comments and according to the example below).

The App should then re-render. It should pass the necessary information from its state to the Lists component, which will then pass it to its List components, which can then render each ListItem with the appropriate values.


Part 3. Marking a ListItem

Certain lists, such as To-Dos or grocery lists, would be greatly improved by the ability to “mark” an item as complete or purchased.

Implement the ListItem.handleClick function so that it is invoked when the user clicks on the content in the ListItem, i.e., within the <span> element. The function should alternate the color of the text in the ListItem between black and gray.
