import React, { useState } from 'react';
import './App.css';

function App() {
  const [cart, setCart] = useState([]);

  const products = [
    { id: 1, name: 'Product 1', price: 10, image: 'product1.jpg', rating: 4 },
    { id: 2, name: 'Product 2', price: 20, image: 'product2.jpg', rating: 3 },
    { id: 3, name: 'Product 3', price: 15, image: 'product3.jpg', rating: 5 },
    // Add more products as needed
  ];

  const addToCart = (product) => {
    setCart([...cart, product]);
  };

  const removeFromCart = (productId) => {
    setCart(cart.filter(item => item.id !== productId));
  };

  return (
    <div className="App">
      <header className="navbar">
        <div className="search-bar">
          <input type="text" placeholder="Search..." />
        </div>
        <div className="categories">
          {/* Category filter options */}
          <button>All</button>
          <button>Category 1</button>
          <button>Category 2</button>
          {/* Add more category buttons as needed */}
        </div>
      </header>
      <main>
        <div className="product-list">
          {products.map(product => (
            <div className="product-card" key={product.id}>
              <img src={product.image} alt={product.name} />
              <h3>{product.name}</h3>
              <p>Price: ${product.price}</p>
              <p>Rating: {product.rating}</p>
              <div className="quantity">
                <button onClick={() => addToCart(product)}>Add to Cart</button>
              </div>
            </div>
          ))}
        </div>
      </main>
      <aside className="cart">
        <h2>Shopping Cart</h2>
        <ul>
          {cart.map(item => (
            <li key={item.id}>
              <span>{item.name}</span>
              <button onClick={() => removeFromCart(item.id)}>Remove</button>
            </li>
          ))}
        </ul>
      </aside>
    </div>
  );
}

export default App;
