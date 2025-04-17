[[Django]]

views are functions which return html file means return what needs to be viewed

so basically we have 
project level
app level

```python
# we declare views in this file
view.py
```

```python
# Http Response object is imp as it sets other attr like get, streaming
def function1(request):
    return HttpResponse("hi")


# if mulitple functions are declared with same name 
# than the later one will be executed
def function1(request):
    return HttpResponse("hiiii")
```

