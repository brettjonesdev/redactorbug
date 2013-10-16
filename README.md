redactorbug
===========

Calling r.redactor('set', r.redactor('get')) repeatedly with a simple body like "ABC" causes an extra space to get added to the text each time 'set' is called.  

For instance, 
```
<p>
   ABC
</p>
```

turns into 
```
<p>
    ABC
</p>
```

etc. until you wind up with something like this:

```
<p>
                                          ABC
</p>
```
