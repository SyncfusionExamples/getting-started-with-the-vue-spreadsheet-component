<script>
  import { SpreadsheetComponent, SheetsDirective, SheetDirective,
      RangesDirective, RangeDirective, ColumnsDirective,
      ColumnDirective } from '@syncfusion/ej2-vue-spreadsheet';
  import datasource from './default.json';
  export default{
    components: {
      'ejs-spreadsheet': SpreadsheetComponent,
      'e-sheets': SheetsDirective,
      'e-sheet': SheetDirective,
      'e-ranges': RangesDirective,
      'e-range': RangeDirective,
      'e-columns': ColumnsDirective,
      'e-column': ColumnDirective
    },
    data(){
      return{
        data: datasource.defaultData,
        customWidth: 130,
        openUrl: 'https://services.syncfusion.com/vue/production/api/spreadsheet/open',
        saveUrl: 'https://services.syncfusion.com/vue/production/api/spreadsheet/save'
      }
    }
  }
</script>

<template>
  <div>
    <ejs-spreadsheet :openUrl="openUrl" :saveUrl="saveUrl">
      <e-sheets>
        <e-sheet>
          <e-columns>
            <e-column :width="customWidth"></e-column>
            <e-column :width="customWidth"></e-column>
            <e-column :width="customWidth"></e-column>
            <e-column :width="customWidth"></e-column>
            <e-column :width="customWidth"></e-column>
            <e-column :width="customWidth"></e-column>
          </e-columns>
          <e-ranges>
            <e-range :dataSource="data"></e-range>
          </e-ranges>
        </e-sheet>
      </e-sheets>
    </ejs-spreadsheet>
  </div>
</template>

<style>
  @import "../node_modules/@syncfusion/ej2-base/styles/material.css";
  @import "../node_modules/@syncfusion/ej2-buttons/styles/material.css";
  @import "../node_modules/@syncfusion/ej2-dropdowns/styles/material.css";
  @import "../node_modules/@syncfusion/ej2-inputs/styles/material.css";
  @import "../node_modules/@syncfusion/ej2-navigations/styles/material.css";
  @import "../node_modules/@syncfusion/ej2-popups/styles/material.css";
  @import "../node_modules/@syncfusion/ej2-splitbuttons/styles/material.css";
  @import "../node_modules/@syncfusion/ej2-grids/styles/material.css";
  @import "../node_modules/@syncfusion/ej2-vue-spreadsheet/styles/material.css";
</style>
