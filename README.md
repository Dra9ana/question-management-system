# Questions Management System

This repository contains a Questions Management System, implemented in C++, which allows users to manage questions and their associated answers through a console interface. Users can add, search, edit, and delete questions and answers, as well as manage ratings for each answer.

## Project Overview

The main features of this system include:
- Adding new questions and answers
- Searching for questions and answers
- Incrementing ratings for answers
- Displaying all questions and their associated answers
- Deleting questions and their answers
- Sorting and printing ratings of answers

## Data Structure

The Questions Management System utilizes **m-ary trees** to organize questions and answers efficiently. Each question can have multiple comments (answers), and each comment can have replies, forming a tree structure. This design allows for:
- Efficient storage of questions and comments.
- Quick traversal to find questions and answers.
- Pre-order tree traversal method to process the nodes efficiently during operations such as searching and displaying content.

### Error Handling

The system incorporates robust error handling, throwing exceptions in scenarios such as:
- Attempting to delete a non-existent question or comment.
- Searching for a question or comment that does not exist.
These measures ensure that users are informed of issues during operations.

### Questions Class

- **Adding Questions and Comments**: Users can add questions and comments as direct children in the tree structure.
- **Deleting Questions and Comments**: The class provides methods to delete questions and comments, including their entire subtrees.
- **Traversals**: The `preorderVisit` method is used for various operations, facilitating depth-first traversal through the tree to perform searches, output nodes, and increment ratings.
- **Memory Management**: The destructor calls a method to delete all nodes in the tree, ensuring proper memory management and preventing memory leaks.
- **Operator Overloading**: The class overloads the `operator<<` to provide a user-friendly way to output all questions.
