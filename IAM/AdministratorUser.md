# Create Administrator User

## Object

1. Understand how to create an IAM user
2. Unserstand how to attach policies to an IAM user

## Step

1. Open the IAM console at https://console.aws.amazon.com/iam/

2. In the navigation pane, choose **Users** and choose Add user

3. Enter user name 

4. Select AWS Management Console access in **Access type**

  - Programmatic access: for API, AWS CLI or Tools
  - AWS Management Console access

  Select **Require password reset**

5. Next: Permissions > Next: Tags > Next: Reviews

6. In the **Review** page, check **Permissions summary** and you can see a managed policy **IAMUserChangePassword**

7. Choose **Show** to view user's password.

8. Open your account sign-in page with Incognito mode and sign in to AWS with new account and password

```
https://My_AWS_Account_ID.signin.aws.amazon.com/console/
```

9. Open the EC2 console and check if you could see some error messages in the EC2 dashboard

10. In your root account, open the IAM console and choose **Users**

11. Choose the new user you created and view **Permissions** tab 

    You would see this user has only one permission **IAMUserChangePassword**

12. Choose **Add permissions**  > Attach existing policies directly > select **AdministratorAccess** > Next: Review > Add Permissions

13. Re-sign in your user and open EC2 console

14. Enable MFA for this user

    https://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_mfa_enable_virtual.html#enable-virt-mfa-for-iam-user




## References

- https://docs.aws.amazon.com/zh_tw/IAM/latest/UserGuide/id_users_create.html#id_users_create_console
- https://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_mfa_enable_virtual.html#enable-virt-mfa-for-iam-user