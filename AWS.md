AWS Cloud Computing Course (Cloud Practitioner) 

Identity and Access Management (Global Service): Users & Groups

	⁃	We already used it, since when we created an AWS account, we created a Root Account (Should never be used or shared). 
	⁃	Users are people within organization and can be grouped. Same person can be in different groups (ex: operations, developpers, Audit, etc.)
	⁃	Why do we create groups? Because we want them to use our account, but giving permission to the groups, and not absolute power of our account. Can give permission to a single person, they don’t necessarily need to be in group. This is called an inline policy.
	⁃	Users in groups are assigned JSON documents, called Policies. It has the code inside the JSON document of the permission. 
*IMPORTANT COMMAND FOR TERMINAL: pwd, ls, cd, cat, echo > name.txt, 
IAM policies structure:
	⁃	Version: policy language version and always includes the date of version
	⁃	ID: Identifier of policy (optional)
	⁃	Statement(s): required
	Statements structure:
	⁃	Sid: identifier of the statement (optional)
	⁃	Effect: Allow or Deny
	⁃	Principal: Account/User/Role the policy is applied to
	⁃	Action: List of actions this policy allows/denies
	⁃	Resource: List of resources to which the actions applied to
	⁃	Condition: Conditions for when this policy is in effect
IAM Multi-factor Authentification: To protect users and groups there are two ways
	⁃	Password Policy: minimum password length, specific characters, allow IAM users to change password, password expiration, prevent password re-use. 
	⁃	Multi-Factor Authentification. Password you know + device you own: 
	⁃	google authenticator and Authy support multiple tokens (accounts) for a single device
	⁃	Universal 2nd Factor (U2F)Security Key is a physical device and you’re good to go (Yubikey by Yubico). Support multiple user roots and IAM users.
	⁃	Hardware Key Fob MFA device (Gemalto)
	⁃	Hardware Key FOB MFA device for AWS GovCloud US (SurPassID) 
How can users access AWS?
	⁃	AWS management console (Password + MFA)
	⁃	AWS Command Line Interface (CLI): Protected by Access Keys —> basically a terminal for AWS
	⁃	AWS Software Developer Kit (SDK): Also Protected by Access Keys
Access Key are generated through the AWS Console. Access Key is the user ID, AND SECRET Access Key is the Password
	⁃	We also have CloudShell, which is the same as CLI but instead of the terminal, it’s on the cloud of AWS. 


IAM Roles:
	⁃	They’re like the user, that need permissions to do stuff on my behalf. But instead of being real people, they’re other AWS services that need the permissions to make actions on my behalf. 
