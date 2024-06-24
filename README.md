# Project: Personal Profile Page with GraphQL

## Objectives

The primary goal of this project is to learn the GraphQL query language by creating a personalized profile page. You will use the provided GraphQL endpoint to query your own data and display it on your profile page.

## Requirements

### Authentication
1. **Login Page**: Create a login page that authenticates users and retrieves a JWT.
    - The JWT is necessary to access the GraphQL API.
    - Obtain the JWT from the signin endpoint: `https://zone01normandie.org/api/auth/signin`.
    - The login should support:
        - `username:password`
        - `email:password`
    - Display an appropriate error message if the credentials are invalid.
    - Provide a method to log out.

### Profile Page
2. **Profile Information**: Display at least three pieces of information about the user, such as:
    - Basic user identification
    - XP amount
    - Grades
    - Audits
    - Skills

3. **Statistics Section**: Create a section for generating and displaying statistic graphs using SVG. You need to implement at least two different types of graphs. Examples include:
    - XP earned over time
    - XP earned by project
    - Audit ratio
    - Projects PASS and FAIL ratio
    - Piscine (JS/Go) stats
        - PASS and FAIL ratio
        - Attempts for each exercise

### GraphQL Usage
4. **GraphQL Queries**: Use the GraphQL endpoint to fetch data for the profile page.
    - Endpoint: `https://zone01normandie.org/api/graphql-engine/v1/graphql`
    - Make use of different types of GraphQL queries:
        - Normal queries
        - Nested queries
        - Queries with arguments

### Hosting
5. **Host the Profile**: Deploy your profile page on a hosting service like GitHub Pages, Netlify, or any other platform of your choice.

## Instructions

1. **Setup Authentication**:
    - Implement a login page that uses the signin endpoint to get a JWT.
    - Use Basic authentication with base64 encoding to send the credentials.
    - Store the JWT securely and use it for subsequent GraphQL queries.

2. **Design the Profile UI**:
    - Design the profile page to display the chosen pieces of information.
    - Ensure the design is user-friendly and visually appealing.

3. **Implement Statistic Graphs**:
    - Use SVG to create interactive and/or animated graphs.
    - Implement at least two different types of statistic graphs based on the user's data.

4. **Fetch Data Using GraphQL**:
    - Query the user table to get basic user information.
    - Query the transaction table for XP and audit ratio.
    - Query the progress and result tables for grades and progression.
    - Example queries:
        ```graphql
        {
          user {
            id
            login
          }
        }
        ```
        ```graphql
        {
          object(where: { id: { _eq: 3323 }}) {
            name
            type
          }
        }
        ```
        ```graphql
        {
          result {
            id
            user {
              id
              login
            }
          }
        }
        ```

5. **Deploy the Profile Page**:
    - Choose a hosting service and deploy your profile page.
    - Ensure that the hosted page is accessible and functional.

## Learning Outcomes

By completing this project, you will gain knowledge and experience in:
- GraphQL and GraphiQL
- Web authentication and JWT
- Hosting web applications
- UI/UX design principles
- SVG for creating graphs and visualizations

## Additional Resources

- [GraphQL Documentation](https://graphql.org/learn/)
- [JWT Introduction](https://jwt.io/introduction/)
- [SVG Tutorial](https://developer.mozilla.org/en-US/docs/Web/SVG/Tutorial)
- [Hosting on GitHub Pages](https://pages.github.com/)
- [Hosting on Netlify](https://www.netlify.com/)

## Notes

- You are encouraged to explore and use additional features and data available through the GraphQL endpoint.
- Pay attention to the principles of good UI design to enhance user experience.
- Make sure to test your profile page thoroughly before deployment.

## Author

This project is created by Jean Marie Murenzi. You can find more about the author and the project [here](https://zone01normandie.org/git/jmurenzi/graphql/_new/master/).