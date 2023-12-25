# React.js-Todo-List-App
Simple Todo List application using React.js.
import React, { useState } from 'react';

function TodoApp() {
    const [todos, setTodos] = useState([]);
    const [newTodo, setNewTodo] = useState('');

    const addTodo = () => {
        setTodos([...todos, newTodo]);
        setNewTodo('');
    };

    return (
        <div>
            <ul>
                {todos.map((todo, index) => (
                    <li key={index}>{todo}</li>
                ))}
            </ul>
            <input
                type="text"
                value={newTodo}
                onChange={(e) => setNewTodo(e.target.value)}
            />
            <button onClick={addTodo}>Add Todo</button>
        </div>
    );
}

export default TodoApp;
