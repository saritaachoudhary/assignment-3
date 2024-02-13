/* App.css */
.App {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin: 20px;
}

.App-header {
  background-color: #333;
  color: white;
  padding: 20px;
  width: 100%;
  text-align: center;
}

.App-main {
  display: flex;
  justify-content: center;
}

.product-list {
  display: flex;
  flex-wrap: wrap;
}

.product-card {
  border: 1px solid #ccc;
  border-radius: 5px;
  margin: 10px;
  padding: 10px;
  width: 200px;
  text-align: center;
}

.product-card img {
  max-width: 100%;
  border-radius: 5px;
}

.App-sidebar {
  background-color: #f4f4f4;
  padding: 20px;
  border-radius: 5px;
  margin-top: 20px;
}

.App-sidebar h2 {
  margin-top: 0;
}

.App-sidebar ul {
  list-style-type: none;
  padding: 0;
}

.App-sidebar li {
  display: flex;
  justify-content: space-between;
  margin-bottom: 5px;
}

.App-sidebar button {
  background-color: #dc3545;
  color: white;
  border: none;
  border-radius: 5px;
  padding: 5px 10px;
  cursor: pointer;
}


