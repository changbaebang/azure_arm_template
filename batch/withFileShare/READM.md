# Create a Batch Account with FileShare

This template creates a Storage Account and FileShare

[![Deploy to Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fchangbaebang%2Fazure_arm_template%2Fmain%2Fbatch%2FwithFileShare%2Fazuredeploy.json)


relativeMountPath should not start with `/` and sould be only single depth.  
- `S` is OK
- `/S` is notavailable
- `S/S` is not available


if relativeMountPath is `/<account name>/<share name>`, not found error would be occured for `/mnt/batch/task/fsmounts/fshare-/<account name>/<share name>.log`.  

if relativeMountPath is `<account name>/<share name>`, not found error would be occured for `/mnt/batch/task/fsmounts/<account name>/<share name>.log`.  

