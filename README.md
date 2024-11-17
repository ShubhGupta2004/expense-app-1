
# Expense Tracker App

This is a simple **Expense Tracker** web application builts using:
- **Frontend:** React.js
Link to  our App : [Our App ](https://pw-expense-app-1.vercel.app/).

## Images
![Screenshot 2024-10-01 203836](https://github.com/user-attachments/assets/11050aaa-8b77-4124-93b6-b15a9195de93)
![Screenshot 2024-10-01 203713](https://github.com/user-attachments/assets/533aea94-b69c-4d4f-b388-50a3193140a6)
![Screenshot 2024-10-01 203737](https://github.com/user-attachments/assets/97b07f4f-bbb4-48ed-8a50-ac40bd17fd85)
![Screenshot 2024-10-01 203836](https://github.com/user-attachments/assets/45a30836-1450-403e-9f65-0177dab47ccb)



## Features
- Add and track expenses
- Categorize expenses

## Project Structure

```
.
├──
├── 
│   ├── src
│   │   ├── components    # React components
│   │   ├── pages         # Pages like Dashboard, Add Expense
│   │   ├── App.js        # Main React app
│   └── package.json      # Frontend dependencies
├── README.md
└── package.json          # Backend dependencies
```

## Prerequisites
1. **Node.js** installed
2. **MongoDB** (or PostgreSQL)
3. **React.js**

### Backend Installation
1. Navigate to the `backend` folder.
2. Install dependencies:
    ```bash
    npm install
    ```
3. Create a `.env` file for environment variables:
    ```bash
    MONGO_URI=mongodb+srv://<username>:<password>@cluster0.mongodb.net/expense_tracker
    PORT=5000
    ```
   If you're using PostgreSQL, replace this with the corresponding PostgreSQL connection URI.

4. Start the backend server:
    ```bash
    npm start
    ```

### Frontend Installation
1. Navigate to the `frontend` folder.
2. Install dependencies:
    ```bash
    npm install
    ```
3. Update `src/config.js` with your backend URL:
    ```js
    export const API_URL = 'http://localhost:5000';  // Update this to your backend address
    ```

4. Start the frontend development server:
    ```bash
    npm start
    ```

### API Endpoints

- `GET /expenses`: Fetch all expenses
- `POST /expenses`: Add a new expense
- `GET /expenses/:id`: Fetch a single expense by ID
- `PUT /expenses/:id`: Update an expense by ID
- `DELETE /expenses/:id`: Delete an expense by ID

## Deploying the App

### Deployment on Heroku (Backend)

1. Create a Heroku account and install the [Heroku CLI](https://devcenter.heroku.com/articles/heroku-cli).
2. Inside the `backend` folder, initialize a git repository:
    ```bash
    git init
    ```
3. Commit your changes:
    ```bash
    git add .
    git commit -m "Initial commit"
    ```
4. Create a Heroku app:
    ```bash
    heroku create expense-tracker-backend
    ```

5. Push your code to Heroku:
    ```bash
    git push heroku master
    ```
6. Your backend will be deployed at `https://<your-app-name>.herokuapp.com`.

### Deployment on Vercel (Frontend)

1. Create an account on [Vercel](https://vercel.com/) and install the [Vercel CLI](https://vercel.com/docs/cli).
2. Inside the `frontend` folder, deploy the app:
    ```bash
    vercel
    ```
3. Follow the CLI prompts to deploy your frontend app. Once completed, your frontend will be live on a Vercel-provided URL.

### Environment Variables for Frontend

You can set the backend API URL by creating a `.env` file at the root of your `frontend` folder:
```
REACT_APP_API_URL=https://<your-backend-url>
```

## Conclusion
You now have a working **Expense Tracker App** with both frontend and backend deployed. The app supports adding, viewing, and categorizing expenses, and provides expense summaries.
