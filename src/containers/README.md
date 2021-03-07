# Containers [Smart Components]

**Smart Components** (or, **Container Components**) have the responsibility of being smart. They are the ones that keep track of state and care about how the app works.

Using the container design pattern, the container components are separated from the presentation components and each handles their own side of things. The container components do the heavy lifting and pass the data down to the presentational component as props.

Smart or Container Components are *hooks* or *class-based components* and have their own state defined.

```
    class App extends Component {
        contructor(props) {
            super(props);
            this.state = {
                name: [ ]
            };
        };
    };
```

These components also often contain other callback functions that are used to update the state and gets passed down to their child components as props.