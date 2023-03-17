---  
share: true  
title: "Django REST Framework"  
comments: true  
---  
up [∴ Python](./%E2%88%B4-Python.md)  
  
# Django REST Framework  
Django REST Framework -- **DRF** -- is a toolkit for building web APIs with **Django**. It provides tools for serializing data, routing, permissions, and more. Instead of using **Django** to build a form-based multipage site, **DRF** helps you to build a consistent API that frontend apps can consume.  
  
## Serializers  
**Serializers** can be defined as classes with a bit of metadata that explains what parts of an existing **Django** model should be exposed. They are the big win in **DRF** for me --- the eliminate all the code I would have to write to convert model data to JSON. Example:  
  
```python  
class CoffeeSerializer(serializers.ModelSerializer):  
	class Meta:  
		model = Coffee  
		fields = ["origin", "date", "rating" ]  
```  
  
## Views  
**Views** can also be defined as classes that expose a **Serializer** and provide a default queryset:  
  
```python  
class CoffeeViewSet(viewsets.ModelViewSet):  
    """  
    API endpoint that allows Coffee models to be viewed.  
    """  
    queryset = Coffee.objects.all()  
    serializer_class = CoffeeSerializer  
```  
  
The `get_queryset` method can be overridden to customize how the view is filtered:  
  
```python  
class ReviewList(generics.ListAPIView):  
     """  
    API endpoint that allows reviews to be viewed by   
    coffee and reviewer.  
    """  
  
	serializer_class = ReviewSerializer  
  
    def get_queryset(self):  
        coffee_id = self.kwargs["coffee"]  
        coffee = Coffee.objects.get(id=coffee_id)  
        reviewers = self.request.query_params.get("reviewer")  
  
        return Reviews.objects.filter(  
            coffee=coffee, reviewer=reviewer  
        )  
```  
  
