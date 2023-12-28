##  Reference for nextpy/frontend/components/chakra/layout/container(Generated by a LLM. Pending Review)

# Container Component

The `Container` component in Nextpy is designed to help you structure the layout of your application by providing a wrapping element that can center and contain its children elements. This component is part of Nextpy's Chakra UI integration, which provides a suite of UI components styled according to Chakra UI's design system.

## Anatomy

To use the `Container` component, you can simply import it from the Nextpy library and add it to your application. Here's a basic example of how to use the `Container` component:

```python
from nextpy.components.chakra.layout import Container

def app():
    return Container.create(
        'Your content goes here',
        center_content=True,
        style=Style(padding="16px", border="1px solid #ccc")
    )
```

In this example, the `Container` is used to wrap a simple text content, centering it and applying some padding and a border for styling.

### Advanced Usage

For more complex scenarios, you can include multiple child components, custom attributes, and event handlers within the `Container`:

```python
from nextpy.components.chakra.layout import Container
from nextpy.frontend.components.basic import Text

def app():
    return Container.create(
        Text.create('Hello, Nextpy!'),
        Text.create('Another line of text.'),
        center_content=True,
        style=Style(padding="24px", background="whitesmoke"),
        on_click=lambda event: print('Container clicked!'),
        custom_attrs={'data-custom': 'value'}
    )
```

## Components

The `Container` component accepts several props and event handlers that allow you to customize its behavior and appearance:

- **center_content** (Optional[Union[Var[bool], bool]]): Centers the child elements if set to `True`.
- **style** (Optional[Style]): Allows you to apply custom styles to the `Container`.
- **key** (Optional[Any]): A unique key that can be used to differentiate components in a list.
- **id** (Optional[Any]): The HTML element ID for the component.
- **class_name** (Optional[Any]): The CSS class name for the component.
- **autofocus** (Optional[bool]): If `True`, the component will be focused on page load.
- **custom_attrs** (Optional[Dict[str, Union[Var, str]]]): Custom attributes for the HTML element.

### Event Handlers

- **on_blur**
- **on_click**
- **on_context_menu**
- **on_double_click**
- **on_focus**
- **on_mount**
- **on_mouse_down**
- **on_mouse_enter**
- **on_mouse_leave**
- **on_mouse_move**
- **on_mouse_out**
- **on_mouse_over**
- **on_mouse_up**
- **on_scroll**
- **on_unmount**

Each event handler accepts a function or a `BaseVar` that defines the behavior when the event is triggered.

## Notes

- Ensure that the `center_content` prop is used judiciously as it may affect the layout of your application.
- When using event handlers, remember to manage state and side effects appropriately to avoid unexpected behavior.

## Best Practices

- Use the `Container` component to manage the layout and alignment of its child elements effectively.
- Apply the `style` prop to customize the `Container`'s appearance, but avoid inline styles that can cause performance issues; prefer using CSS classes when possible.
- Leverage the event handlers to create interactive elements, but ensure they are not causing performance bottlenecks or unnecessary re-renders.
- Keep the `Container`'s usage simple and clear, avoiding deeply nested structures that may complicate the application's architecture.

Remember to check the Nextpy documentation for updates, as the library may introduce new props and features that enhance the `Container` component's capabilities.