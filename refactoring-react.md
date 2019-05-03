# Refactoring react
### From good code to great code

- don't use props in state/constructor
- Components should take props which handle behaviour not interaction
- feature envy - when a feature is too interested in children's behaviour
- spread props down reusable components to allow for flexibility
- order of props is important
- dont mix, controlled/uncontrolled state
- single responsibility: components should do one thing well, delegate to higher up when can
- can pull logic that doesn't fit main responsibility into HOCs
- Sid says no tests is a code smell :eyes:
- Noone has time for 100% coverage
- Hooks +1 
- using children > text/messge props is optimised for change/flexibility
```jsx
React.Children.map(
  props.children,
  function (child) {
    // ...
    return child,
  }
)
```
above can do some cool prop drilling, BUT context is a lot neater. 
```jsx
<FormContext.Provider>
  <Form>
    {/**  ??? */} 
  </Form>
</FormContext.Provider>
```
? check twitter for cloneElement vs context cases
sid.studoi/refactoring

- Minimal API surface area