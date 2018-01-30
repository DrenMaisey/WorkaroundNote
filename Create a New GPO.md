# Create a New GPO

## First Step
1. Open Group Policy Editor in you DC
2. Right click over group policy objects
3. New
4. Input the name of the policy
5. Click on the new object to start modifing

## Something to rememeber
1. Remember that if the policy is a User Policy* must be applied to OU of user and if is a computer policy must be applied to a computer OU


2. If you modify the security Filter adding group or user to specify to who the Policy will be applied (removing the authenticated user Group),
[Safety Filters](https://github.com/DrenMaisey/WorkaroundNote/blob/master/newGPO/FiltriDiSicurezza.png "Safety Filters")


You must add in the Delgation Tab the **Domain Computer** group in order apply the policy to the user

[Delegation](https://github.com/DrenMaisey/WorkaroundNote/blob/master/newGPO/Delega.png "Delegation")



*Diff between User or computer Policy 

[UserOrComputer](https://github.com/DrenMaisey/WorkaroundNote/blob/master/newGPO/UserOrComputerPolicy.png "UserOrComputer")