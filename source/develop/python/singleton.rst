Singleton Python
================

.. code-block:: python

    # Borg Pattern
    class Earth:
        __dict = {}
        def __init__(self):
            self.__dict__ = self.__dict

    e1 = Earth()
    e2 = Earth()
    e1.population = 30000000
    print e2.population



    # or with Singleton decorator (https://www.python.org/dev/peps/pep-0318/)

    def singleton(cls):
        instances = {}
        def getinstance():
            if cls not in instances:
                instances[cls] = cls()
            return instances[cls]
        return getinstance

    @singleton
    class Earth:
        pass

    e1 = Earth()
    e2 = Earth()
    e1.population = 30000000
    print e2.population
