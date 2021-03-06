To export or print the Funnel, a user clicks the *"Exporting/Printing"* button and selects a command from the drop-down menu. The **Print** command opens the browser's **Print** window that lets the user select preferred printing settings and send the print job to the printer. The other commands save a file of the selected format in the user's local storage.

![Funnel Export Menu](/images/Funnel/visual_elements/export-menu.png)

You can enable both exporting and printing by setting the [export](/api-reference/20%20Data%20Visualization%20Widgets/BaseWidget/1%20Configuration/export '/Documentation/ApiReference/UI_Components/dxFunnel/Configuration/export/').**enabled** property to **true**. If you need only exporting to be available to the user, disable printing by assigning **false** to the **export**.[printingEnabled](/api-reference/20%20Data%20Visualization%20Widgets/BaseWidget/1%20Configuration/export/printingEnabled.md '/Documentation/ApiReference/UI_Components/dxFunnel/Configuration/export/#printingEnabled') property.

---
##### jQuery

    <!--JavaScript-->$(function() {
        $("#funnelContainer").dxFunnel({
            // ...
            export: {
                enabled: true,
                printingEnabled: false
            }
        });
    });

##### Angular

    <!--HTML--><dx-funnel ... >
        <dxo-export
            [enabled]="true"
            [printingEnabled]="false">
        </dxo-export>
    </dx-funnel>

    <!--TypeScript-->
    import { DxFunnelModule } from "devextreme-angular";
    // ...
    export class AppComponent {
        // ...
    }
    @NgModule({
        imports: [
            // ...
            DxFunnelModule
        ],
        // ...
    })

##### Vue

    <!-- tab: App.vue -->
    <template> 
        <DxFunnel ... >
            <DxExport
                :enabled="true"
                :printing-enabled="false"
            />
        </DxFunnel>
    </template>

    <script>
    import DxFunnel, { DxExport } from 'devextreme-vue/funnel';

    export default {
        components: {
            DxFunnel,
            DxExport
        }
    }
    </script>

##### React

    <!-- tab: App.js -->
    import React from 'react';
    import Funnel, { Export } from 'devextreme-react/funnel';

    class App extends React.Component {
        render() {
            return (
                <Funnel ... >
                    <Export 
                        enabled={true}
                        printingEnabled={false}
                    />
                </Funnel>
            );
        }
    }

    export default App;

---

If you want to restrict the set of formats available for exporting, change the **export**.[formats](/api-reference/20%20Data%20Visualization%20Widgets/BaseWidget/1%20Configuration/export/formats.md '/Documentation/ApiReference/UI_Components/dxFunnel/Configuration/export/#formats') array. You can also specify the default name for the exported file using the [fileName](/api-reference/20%20Data%20Visualization%20Widgets/BaseWidget/1%20Configuration/export/fileName.md '/Documentation/ApiReference/UI_Components/dxFunnel/Configuration/export/#fileName') property.

---
##### jQuery

    <!--JavaScript-->$(function() {
        $("#funnelContainer").dxFunnel({
            // ...
            export: {
                enabled: true,
                formats: ["PNG", "JPEG"],
                fileName: "exported_funnel"
            }
        });
    });

##### Angular

    <!--HTML--><dx-funnel ... >
        <dxo-export
            [enabled]="true"
            [formats]="['PNG', 'JPEG']"
            fileName="exported_funnel">
        </dxo-export>
    </dx-funnel>

    <!--TypeScript-->
    import { DxFunnelModule } from "devextreme-angular";
    // ...
    export class AppComponent {
        // ...
    }
    @NgModule({
        imports: [
            // ...
            DxFunnelModule
        ],
        // ...
    })

##### Vue

    <!-- tab: App.vue -->
    <template> 
        <DxFunnel ... >
            <DxExport
                :enabled="true"
                :formats="exportFormats"
                file-name="exported_funnel"
            />
        </DxFunnel>
    </template>

    <script>
    import DxFunnel, { DxExport } from 'devextreme-vue/funnel';

    export default {
        components: {
            DxFunnel,
            DxExport
        },
        data() {
            return {
                exportFormats: ['PNG', 'JPEG']
            }
        }
    }
    </script>

##### React

    <!-- tab: App.js -->
    import React from 'react';
    import Funnel, { Export } from 'devextreme-react/funnel';

    const exportFormats = ['PNG', 'JPEG'];

    class App extends React.Component {
        render() {
            return (
                <Funnel ... >
                    <Export 
                        enabled={true}
                        formats={exportFormats}
                        fileName="exported_funnel"
                    />
                </Funnel>
            );
        }
    }

    export default App;

---
