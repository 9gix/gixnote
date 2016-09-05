# Setup Magento Extension

1. Disable all cache at `Admin Panel > System > Cache Management`

2. Enable Error Printing, go to `<ProjectDir>/errors`.
   Copy `local.xml.sample` to `local.xml`

3. Decide `ModuleNamespace` and `ModuleName`

4. Let `<ModuleDirectory>` be
   `<ProjectDirectory>/app/code/community/<ModuleNamespace>/<ModuleName>/`.

5. Create [Module Configuration file][1] at  `<ModuleDirectory>/etc/config.xml`


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


6. Activate Module using Initial configuration file.
   `<ProjectDirectory>/app/etc/modules/<ModuleNamespace_ModuleName>.xml`


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


7. Verify The module is added at `System >> Configuration >> Advanced >> Advanced`

8. Plan/Design the Extension structure.

9. Start writing the code, and always include them 
   inside the module configuration file.

1. Learn `modman` for packaging the extension

[1]: http://www.magentocommerce.com/wiki/5_-_modules_and_development/reference/module_config.xml
