---
published: false
---
# React Lifecycle, State, and Props

## Lifecycle

There are 3 phases in a React component lifecycle - mounting, updating, and unmounting. In each phase there are specific lifecycle methods available which are a series of events that happen throughout the mounting, updating, and unmounting of a React component.

I'll list the available methods of each phase below.

1.  Mounting - adding nodes to the DOM
2.  Updating - altering existing nodes in the DOM
3.  Unmounting - removing nodes from the DOM
4.  Error handling - verifying that the code works and is bug free

In the first phase is inserted into the DOM, which then moves into the updating phase. Without the updating phase it would remain as it is initially created in the DOM without taking in any specific state or props. Keep in mind that any components that may help to shape the state and attribute props to one component require the same lifecycle flow. The final phase of unmounting removes a component from the DOM. There is one additional phase that a component may go through which is the error handling phase which results in your code not running due to a bug in your code.

Components may not go through every phase. It's possible for a component to be mounted and unmounted without anything being updated and if there are no errors that phases would also be skipped.

The available lifecycle methods for each phase of a component and are typically called in the order below.

### Mounting

- [constructor()](https://reactjs.org/docs/react-component.html#constructor)
- [static getDerivedStateFromProps()](https://reactjs.org/docs/react-component.html#static-getderivedstatefromprops)
- [render()](https://reactjs.org/docs/react-component.html#render)
- [componentDidMount()](https://reactjs.org/docs/react-component.html#componentdidmount)

### Updating

- [static getDerivedStateFromProps()](https://reactjs.org/docs/react-component.html#static-getderivedstatefromprops)
- [shouldComponentUpdate()](https://reactjs.org/docs/react-component.html#shouldcomponentupdate)
- [render()](https://reactjs.org/docs/react-component.html#render)
- [getSnapshotBeforeUpdate()](https://reactjs.org/docs/react-component.html#getsnapshotbeforeupdate)
- [componentDidUpdate()](https://reactjs.org/docs/react-component.html#componentdidupdate)

### Unmounting

- [componentWillUnmount()](https://reactjs.org/docs/react-component.html#componentwillunmount)

### Error handling

- [static getDerivedStateFromError()](https://reactjs.org/docs/react-component.html#static-getderivedstatefromerror)
- [componentDidCatch()](https://reactjs.org/docs/react-component.html#componentdidcatch)

For additional information about the above methods please refer to <https://reactjs.org/docs/react-component.html>.

## Props

Props are arguments passed into React components similar to how we pass HTML attributes. The data flow in React is unidirectional meaning from parent components to child components.

```javascript
	class ParentComponent extends Component {
		render() {
			return <ChildComponent name='First Child' />;
		}
	}
```

```javascript
	const ChildComponent = (props) => {
		return <p>{props.name}</p>;
	};
```
The above code demonstrates a defined prop of `name` with a text data value of `"First Child"` which we are able to use the the child component via the `(props)` argument. To render the prop we utilize dot notation along with the prop i.e. `{props.name}`. When the component loads it will display the prop as it was passed.

## State

A built in object, State allows components to create and manage their own data. Unlike Props, components cannot pass data with state, but they can create and manage it internally. State is similar to props but it is private and fully controlled by the component.

```javascript
class Test extends React.Component {
	constructor() {
		this.state = {
			id: 1,

			name: 'test',
		};
	}

	render() {
		return (
			<div>
				<p>{this.state.id}</p>

				<p>{this.state.name}</p>
			</div>
		);
	}
}
```
State should not be modified directly, but it can be modified with a special method called `setState()`.

A change in state occurs with user-input, triggering an event, etc. React components with state are rendered based on the data in state. State holds the initial information.