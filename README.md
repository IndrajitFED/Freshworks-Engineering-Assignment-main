##### INDRAJIT SHINDE aka INDRAJITFED
##### Freshworks-Engineering-Assignment
##### [key-value-ds](https://pypi.org/project/key-value-ds/)
##### File based Key-Value datastore

   Task is to Build a file-based  key-value data store that supports the basic CRD (Create, Read, Delete) operations.

**Usage:**

###### Simply First Create an instance
```
import key_value_ds
ds_instance = key_value_ds.get_instance()
```

###### To create an data
```
data_key = 'T_key'
data_value = {"value": 1}  # must be a JSON
time_to_live = 3*1000  # time in milliseconds
ds_instance.create(data_key, data_value, ttl=time_to_live)
```

###### To retrieving the data
```
retrieve_key = 'T_key'
ds_instance.get(retrieve_key)   # returns {"value": 1} if retrieved within 5 seconds else ValueError
```

###### To delete the data
```
key_to_delete = 'T_key'
ds_instance.delete(key_to_delete) 
# key-value is removed from the datastore
```

###### Delete all data
```
ds_instance.delete_all()
```
