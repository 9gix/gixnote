Setup Magento Extension
=======================

#. Disable all cache at ``Admin Panel > System > Cache Management``

#. Decide ``ModuleNamespace`` and ``ModuleName``

#. Let ``<ModuleDirectory>`` be
   ``<ProjectDirectory>/app/code/community/<ModuleNamespace>/<ModuleName>/``.

#. Create Module Configuration 
   ``<ModuleDirectory>/etc/config.xml``

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
        </config>


#. Activate Module for Project.
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

#. Learn ``modman`` for packaging the extension
