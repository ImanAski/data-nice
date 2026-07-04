# Testing

from my old days, I've been taught the 
triple A(Arrange-Act-Assert) pattern. what is it?

## Arrange

This is where we prepare the test data and any 
necessary deps like

```python
user = UserFactory()
service = UserService()
```

## Act

This is where we execute the actual testing

```python
resutl = service.create(user)
```

## Assert

This is where we verify and put the result next 
to our desired behaviour

```python
assert result is not None
```

