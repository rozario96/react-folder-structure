# Dumb Components

**Dumb Components** are also called **Presentational Components** because their only responsibility is to present something to the DOM. Once that is done, the component is done with it.

The component themselves only have a render() method and are often just JavaScript functions. They don't have internal state to manage. They wouldn't know how to change the data they are presenting if they were asked.

```
    const Footer = (props) => {
        return (
            <p>Footer Info</p>
        );
    };  
```
