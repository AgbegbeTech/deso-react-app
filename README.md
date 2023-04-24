# deso-react-app

A simple React app with Deso integration. This is a React app that uses the Deso SDK and React bindings to create a balance component.

## Getting Started

1. Clone the repository
2. Run `npm install` to install the required dependencies
3. Initialize Deso with your node's URL
4. Render the React component to the DOM
5. Enjoy your balance component!

## Usage

To use the Deso balance component in your React app, import the `DesoBalance` component and use it like this:

```jsx
import React from 'react';
import { render } from 'react-dom';
import { Deso } from '@deso/sdk';
import { DesoBalance } from '@deso/react';

const deso = new Deso('http://localhost:8080');

function App() {
  return (
    <div>
      <DesoBalance
        desoNode={deso}
        publicKey="your-public-key"
        onBalanceChange={(balance) => console.log(`New balance: ${balance}`)}
      />
    </div>
  );
}

render(<App />, document.getElementById('root'));
