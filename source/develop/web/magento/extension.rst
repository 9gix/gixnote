Setup Magento Extension
=======================

#. Disable all cache at ``Admin Panel > System > Cache Management``

#. Enable Error Printing, go to ``<ProjectDir>/errors``.
   Copy ``local.xml.sample`` to ``local.xml``

#. Decide ``ModuleNamespace`` and ``ModuleName``

#. Let ``<ModuleDirectory>`` be
   ``<ProjectDirectory>/app/code/community/<ModuleNamespace>/<ModuleName>/``.

#. Create `Module Configuration file`_ at  ``<ModuleDirectory>/etc/config.xml``

    .. code-block:: xml
        :linenos:

        <!-- File: app/code/community/MyCompany/MyProduct/etc/config.xml -->
        <?xml version="1.0" encoding="UTF-8"?>
        <config>
            <modules>
                <MyCompany_MyProduct>
                    <version>0.0.0</version>
                </MyCompany_MyProduct>
            </modules>
            <global>
                <!-- 
                PHP Code declaration
                --------------------
                Define the Model Class and ModelResource definition
                Define the Helper Class
                Define the Block Class
                Define the Resources Setup
                Define the Event Listener or Signal
                -->
            </global>

            <!-- define More Module Configuration here -->

        </config>


#. Activate Module using Initial configuration file.
   ``<ProjectDirectory>/app/etc/modules/<ModuleNamespace_ModuleName>.xml``

    .. code-block:: xml
        :linenos:

        <!-- File: app/etc/modules/MyCompany_MyProduct.xml -->
        <?xml version="1.0" encoding="UTF-8"?>
        <config>
            <modules>
                <MyCompany_MyProduct>
                    <active>true</active>
                    <codePool>community</codePool>
                </MyCompany_MyProduct>
            </modules>
        </config>


#. Verify The module is added at ``System >> Configuration >> Advanced >> Advanced``

#. Plan/Design the Extension structure.

#. Start writing the code, and always include them 
   inside the module configuration file.

#. Learn ``modman`` for packaging the extension

.. _`Module Configuration file`: http://www.magentocommerce.com/wiki/5_-_modules_and_development/reference/module_config.xml
