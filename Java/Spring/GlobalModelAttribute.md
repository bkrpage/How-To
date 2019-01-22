# Create a global Model Attribute

Spring 4, Spring 5

Create a model attribute that can be used among all views without being set in every controller. e.g. Username to be added to the top of each page. Found Here: https://stackoverflow.com/a/33879102

Using an advice class annoted with `@ControllerAdvice` allows the setting of global model attributes:

```
@ControllerAdvice
public class GlobalControllerAdvice {

    @ModelAttribute("user")
    public List<Exercice> populateUser() {
        User user = /* Get your user from service or security context or elsewhere */;
        return user;
    }
}
```

A model attribute named `user` will now be available to be used via `${user}`