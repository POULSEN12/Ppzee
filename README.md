# Ppzee
Creating an expense tracker website involves structuring HTML files for different pages and styling them using CSS. Below, I'll outline the basic structure and styling considerations for each required HTML file and provide an example of how you might organize your project.

### HTML Structure

1. **index.html** (Landing Page)
   
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Expense Tracker - Home</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Expense Tracker</h1>
        <nav>
            <ul>
                <li><a href="register.html">Register</a></li>
                <li><a href="login.html">Login</a></li>
            </ul>
        </nav>
    </header>

    <section class="hero">
        <h2>Welcome to Expense Tracker</h2>
        <p>Track your expenses efficiently with our easy-to-use tool.</p>
    </section>

    <footer>
        <p>&copy; 2024 Expense Tracker. All rights reserved.</p>
    </footer>
</body>
</html>
```

2. **register.html** (Registration Page)

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Register - Expense Tracker</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Register</h1>
    </header>

    <section class="form-container">
        <form action="submit_registration.php" method="POST">
            <label for="username">Username:</label>
            <input type="text" id="username" name="username" required>
            
            <label for="password">Password:</label>
            <input type="password" id="password" name="password" required>

            <button type="submit">Register</button>
        </form>
    </section>

    <footer>
        <p>&copy; 2024 Expense Tracker. All rights reserved.</p>
    </footer>
</body>
</html>
```

3. **login.html** (Login Page)

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Login - Expense Tracker</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Login</h1>
    </header>

    <section class="form-container">
        <form action="login.php" method="POST">
            <label for="username">Username:</label>
            <input type="text" id="username" name="username" required>
            
            <label for="password">Password:</label>
            <input type="password" id="password" name="password" required>

            <button type="submit">Login</button>
        </form>
    </section>

    <footer>
        <p>&copy; 2024 Expense Tracker. All rights reserved.</p>
    </footer>
</body>
</html>
```

4. **add_expense.html** (Add Expense Page)

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Add Expense - Expense Tracker</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Add Expense</h1>
        <nav>
            <ul>
                <li><a href="index.html">Home</a></li>
                <li><a href="view_expense.html">View Expenses</a></li>
            </ul>
        </nav>
    </header>

    <section class="form-container">
        <form action="add_expense.php" method="POST">
            <label for="expense_name">Expense Name:</label>
            <input type="text" id="expense_name" name="expense_name" required>
            
            <label for="amount">Amount:</label>
            <input type="text" id="amount" name="amount" required>

            <label for="category">Category:</label>
            <select id="category" name="category">
                <option value="food">Food</option>
                <option value="transport">Transport</option>
                <option value="shopping">Shopping</option>
                <option value="other">Other</option>
            </select>

            <button type="submit">Add Expense</button>
        </form>
    </section>

    <footer>
        <p>&copy; 2024 Expense Tracker. All rights reserved.</p>
    </footer>
</body>
</html>
```

5. **edit_expense.html** (Edit Expense Page)

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Edit Expense - Expense Tracker</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Edit Expense</h1>
        <nav>
            <ul>
                <li><a href="index.html">Home</a></li>
                <li><a href="view_expense.html">View Expenses</a></li>
            </ul>
        </nav>
    </header>

    <section class="form-container">
        <form action="edit_expense.php" method="POST">
            <label for="expense_name">Expense Name:</label>
            <input type="text" id="expense_name" name="expense_name" required>
            
            <label for="amount">Amount:</label>
            <input type="text" id="amount" name="amount" required>

            <label for="category">Category:</label>
            <select id="category" name="category">
                <option value="food">Food</option>
                <option value="transport">Transport</option>
                <option value="shopping">Shopping</option>
                <option value="other">Other</option>
            </select>

            <button type="submit">Update Expense</button>
        </form>
    </section>

    <footer>
        <p>&copy; 2024 Expense Tracker. All rights reserved.</p>
    </footer>
</body>
</html>
```

6. **view_expense.html** (View Expense Page)

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>View Expenses - Expense Tracker</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>View Expenses</h1>
        <nav>
            <ul>
                <li><a href="index.html">Home</a></li>
                <li><a href="add_expense.html">Add Expense</a></li>
            </ul>
        </nav>
    </header>

    <section class="expense-list">
        <h2>Expense List</h2>
        <ul>
            <li>
                <span class="expense-name">Lunch</span>
                <span class="amount">$15.50</span>
                <span class="category">Food</span>
                <a href="edit_expense.html">Edit</a>
                <a href="#">Delete</a>
            </li>
            <!-- Repeat li elements for each expense -->
        </ul>
    </section>

    <footer>
        <p>&copy; 2024 Expense Tracker. All rights reserved.</p>
    </footer>
</body>
</html>
```

### CSS Styling (styles.css)

```css
/* General Styles */
body {
    font-family: Arial, sans-serif;
    line-height: 1.6;
    background-color: #f0f0f0;
    margin: 0;
    padding: 0;
}

header {
    background-color: #333;
    color: #fff;
    padding: 10px 20px;
    display: flex;
    justify-content: space-between;
    align-items: center;
}

header h1 {
    margin: 0;
}

nav ul {
    list-style-type: none;
    margin: 0;
    padding: 0;
}

nav ul li {
    display: inline;
    margin-right: 20px;
}

nav ul li a {
    color: #fff;
    text-decoration: none;
}

section {
    padding: 20px;
    margin: 20px;
    background-color: #fff;
    border-radius: 5px;
    box-shadow: 0 0 10px rgba(0,0,0,0.1);
}

form {
    max-width: 400px;
    margin: auto;
}

label {
    display: block;
    margin-bottom: 10px;
}

input[type="text"],
input[type="password"],
select {
    width: 100%;
    padding: 10px;
    margin-bottom: 15px;
    border: 
