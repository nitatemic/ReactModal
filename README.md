# @nitatemic/ReactModal

[![npm version](https://img.shields.io/npm/v/@nitatemic/reactmodal.svg)](https://www.npmjs.com/package/@nitatemic/reactmodal)

A simple modal component for React.

## Installation

You can install the package using npm or yarn:

```
npm install @nitatemic/ReactModal
```
or
```
yarn add @nitatemic/ReactModal
```

## Usage

```jsx
import React, { useState } from 'react';
import Modal from '@nitatemic/ReactModal';

const App = () => {
    const [modalOpen, setModalOpen] = useState(false);

    const openModal = () => {
        setModalOpen(true);
    };

    const closeModal = () => {
        setModalOpen(false);
    };

    return (
        <div>
            <button onClick={openModal}>Open Modal</button>
            <Modal isOpen={modalOpen} onClose={closeModal} displayCross>
                <h2>Modal Content</h2>
                <p>This is the content of the modal.</p>
            </Modal>
        </div>
    );
};

export default App;

```

[![Open in StackBlitz](https://developer.stackblitz.com/img/open_in_stackblitz.svg)](https://stackblitz.com/edit/nitatemicreactmodal?file=src%2FApp.jsx)

## Styling

The Modal component provides a default styling, but you can customize it to fit your application's design. Here is the
default CSS that you can override:

```css
.modal-overlay {
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background-color: rgba(0, 0, 0, 0.5);
    display: flex;
    align-items: center;
    justify-content: center;
}

.modal-background {
    background-color: #fff;
    border-radius: 4px;
    padding: 20px;
    max-width: 400px;
    max-height: 80vh;
    overflow-y: auto;
}

.modal-cross {
    position: absolute;
    top: 10px;
    right: 10px;
    background: none;
    border: none;
    font-size: 24px;
    cursor: pointer;
}
```

## Props

The Modal component accepts the following props:

 - **isOpen** (boolean): Determines whether the modal is open or closed.
 - **onClose** (function): Callback function to be executed when the modal is closed.
 - **displayCross** (boolean): Determines whether to display the cross icon to close the modal. (If you prefer to use your own close button, set this to false.

## License

This project is licensed under the MIT License - see the LICENSE file for details.
