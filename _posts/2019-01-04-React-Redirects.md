# Redirects
#react/routing #react/redirects

### Simple Redirecting
React router Dom supports redirects, which allow you to redirect the users when they try to access a certain path.

Firstly, import Redirect from react-router-dom:

```javascript
import {Route, NavLink, Switch, Redirect} from ‘react-router-dom’;
```

And then use in a Switch element as below:

> Redirect must be used within the Switch element  

``` jsx
<Switch>
	<Redirect from=“/” to=“/posts” />
</Switch>
```

This feature does not load content like the standard Route elements, but instead loads a redirect

-----

### Conditional Redirects
Conditional redirects can be very useful in cases where you need to redirect a user after an action or event has been executed.

For example, we can redirect a user after a post has been submitted:

Firstly, import Redirect from `react-router-dom`
``` javascript
import {Redirect} from 'react-router-dom'
```

Next, we will need to add know whether the form has been submitted or not by adding the submitted attribute to our state:

``` javascript
    state = {
        submitted: false,
    };
```

Then once the event, e.g a button click is executed, change submitted in the state:

``` javascript
                this.setState({submitted:true});
```

Finally, within the render method, check if submitted is true, and if so redirect the user:

``` javascript
    render() {
        let redirect = null;
        if (this.state.submitted){
            redirect = <Redirect to="/posts" />;
        }
```

Simply add `{redirect}` into your JSX, which will either return null or the redirect 🎉

-----

### Using the History Prop
 #React/history

Redirect actually **replaces** the current page on the stack, which means if the user presses the back button, they won’t be able to go back. If you want the users to be able to go back, use the following:

> Doing this will eradicate the need for setting the state and adding the {redirect} JSX. If this method is preferred in general, `.replace` can be used instead of `.push` to achieve the above in simpler way  

``` javascript
    // Old: Users CANNOT go back
    // this.setState({submitted:true});

    // Users CAN go back
    this.props.history.push('/posts');
```