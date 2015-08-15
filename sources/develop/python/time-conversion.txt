Time Conversion
===============

"24hr" -> "12hr" format 

.. code-block:: python

    import time

    t24 = "23:30"
    t12 = time.strftime("%I:%M %p", time.strptime(t24, "%H:%M"))
    assert t12 == "11:30 pm"
