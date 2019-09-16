# ABAP BAPI Business Object Class Generator

This is a SAP Executable ABAP program to generate Business Object ABAP class based on the BAPIs of a SAP Business Object.

For example a Material Master Business Object class can be generated based on the BAPIs
- Create : BAPI_MATERIAL_SAVEDATA
- Read   : BAPI_MATERIAL_GET_DETAIL
- Update : BAPI_MATERIAL_SAVEDATA

For more information on how it works, see SAP Blog: ABAP BAPI BO Class Generator
https://blogs.sap.com/2019/08/27/abap-bapi-bo-class-generator/

# Versions
1.0 Initial version

1.1 Bugfix version
- bapiret1_t renamed to bapiret1_tab

1.2 Change
- Generate class interface functionality added. See selection screen check box field "Generate class interface".
- Selection screen better aranged.
- NON-cru BAPIs added. (CRU = Create, Read, Update)
- Improved code generation. In create method first the importing parameter is copied to a local variable to overcome a dump if BAPI wants to change the parameter. Method contained an unused local deep structure variable if no exporting were available except the return variable. De return variable are handled by separate local variables.
- Refactoring the tool code.
