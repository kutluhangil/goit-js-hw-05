<h1>📘 JavaScript Homework 5</h1>

<p>This repository contains solutions for <strong>4 tasks</strong> focused on <strong>array methods, chaining, and data transformation</strong> in JavaScript. Each task is implemented in a separate file (<code>task-1.js</code>, <code>task-2.js</code>, <code>task-3.js</code>, <code>task-4.js</code>).</p>

<hr>

<h2>🔹 Task 1: User Names (<code>task-1.js</code>)</h2>

<p>A function that returns an array of user names from an array of user objects.</p>

<pre><code>const getUserNames = (users) => {
  return users.map(user => user.name);
};
</code></pre>

<p>✅ <strong>Test Results</strong></p>

<pre><code>getUserNames([
  { name: "Moore Hensley", email: "moorehensley@indexia.com", balance: 2811 },
  { name: "Sharlene Bush", email: "sharlenebush@tubesys.com", balance: 3821 },
  { name: "Ross Vazquez", email: "rossvazquez@xinware.com", balance: 3793 },
]);
// ["Moore Hensley", "Sharlene Bush", "Ross Vazquez"]
</code></pre>

<hr>

<h2>🔹 Task 2: Users With Specific Friend (<code>task-2.js</code>)</h2>

<p>A function that filters and returns all users who have a specific friend in their <code>friends</code> list.</p>

<pre><code>const getUsersWithFriend = (users, friendName) => {
  return users.filter(user => user.friends.includes(friendName));
};
</code></pre>

<p>✅ <strong>Test Results</strong></p>

<pre><code>getUsersWithFriend([
  { name: "Sharlene Bush", friends: ["Briana Decker", "Sharron Pace"] },
  { name: "Sheree Anthony", friends: ["Goldie Gentry", "Briana Decker"] },
], "Briana Decker");
// [
//   { name: "Sharlene Bush", friends: ["Briana Decker", "Sharron Pace"] },
//   { name: "Sheree Anthony", friends: ["Goldie Gentry", "Briana Decker"] }
// ]
</code></pre>

<hr>

<h2>🔹 Task 3: Sort by Friend Count (Descending) (<code>task-3.js</code>)</h2>

<p>A function that sorts users in descending order by their number of friends. Uses <code>toSorted()</code> to avoid mutating the original array.</p>

<pre><code>const sortByDescendingFriendCount = (users) => {
  return users.toSorted((a, b) => b.friends.length - a.friends.length);
};
</code></pre>

<p>✅ <strong>Test Results</strong></p>

<pre><code>sortByDescendingFriendCount([
  { name: "Ross Vazquez", friends: ["A", "B", "C"] },
  { name: "Sharlene Bush", friends: ["A", "B"] },
  { name: "Moore Hensley", friends: ["A"] },
]);
// [
//   { name: "Ross Vazquez", friends: ["A", "B", "C"] },
//   { name: "Sharlene Bush", friends: ["A", "B"] },
//   { name: "Moore Hensley", friends: ["A"] }
// ]
</code></pre>

<hr>

<h2>🔹 Task 4: Total Balance by Gender (<code>task-4.js</code>)</h2>

<p>A function that calculates the total balance of users by gender using method chaining (<code>filter</code> → <code>map</code> → <code>reduce</code>).</p>

<pre><code>const getTotalBalanceByGender = (users, gender) => {
  return users
    .filter(user => user.gender === gender)
    .map(user => user.balance)
    .reduce((sum, balance) => sum + balance, 0);
};
</code></pre>

<p>✅ <strong>Test Results</strong></p>

<pre><code>const users = [
  { name: "Moore Hensley", gender: "male", balance: 2811 },
  { name: "Sharlene Bush", gender: "female", balance: 3821 },
  { name: "Ross Vazquez", gender: "male", balance: 3793 },
  { name: "Elma Head", gender: "female", balance: 2278 },
  { name: "Carey Barr", gender: "male", balance: 3951 },
  { name: "Blackburn Dotson", gender: "male", balance: 1498 },
  { name: "Sheree Anthony", gender: "female", balance: 2764 },
];

getTotalBalanceByGender(users, "male");
// 12053

getTotalBalanceByGender(users, "female");
// 8863
</code></pre>

<hr>

<h2>📌 Summary & Reflection</h2>

<p>With this homework, you practiced:</p>

<ul>
  <li>Extracting data from objects using <code>map()</code></li>
  <li>Filtering arrays with <code>filter()</code> and <code>includes()</code></li>
  <li>Sorting arrays immutably using <code>toSorted()</code></li>
  <li>Aggregating numerical data with <code>reduce()</code></li>
  <li>Writing clean, functional, and non-mutating JavaScript code</li>
</ul>

<p>These exercises strengthen your understanding of <strong>array methods</strong> and help you write efficient, readable, and modern JavaScript 🚀</p>

<hr>

<h2>📌 Overview</h2>

<ul>
  <li><strong>Task 1:</strong> Extract user names with <code>map()</code></li>
  <li><strong>Task 2:</strong> Find users with a specific friend using <code>filter()</code> and <code>includes()</code></li>
  <li><strong>Task 3:</strong> Sort users by friend count using <code>toSorted()</code></li>
  <li><strong>Task 4:</strong> Calculate total balance by gender using <code>filter()</code>, <code>map()</code>, and <code>reduce()</code></li>
</ul>
