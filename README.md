# aws-sso
Single Sign on configuration / Automation

# AWS SSO Automation?
This is an example repo for AWS SSO permission set automation. It allows you to create permission sets
and deploy them automaticly through pipelines

Benifits of this
- Easy to keep track of changes / versions
- Faster time to deploy (no manual steps)
- Master is your source of truth
- Easy to manage
- Easy to deploy

What do you need to do to get started?

1. Fork this repo into your own Github account
2. Go into each of the files and change
 - ExampleCompany to your company name (Case Sensitive)
 - Change example to your company name (Case Sensitive)
3. Run the codepipeline.yml in your devops / codepipleine central account 
4. Run the master.yml in your master account (Master Payer)
5. Run the pipeline.yml in your devops / codepipleine central account
6. Accept Codestar connection (See https://aws.amazon.com/codestar/)
7.  Run the pipeline!

Note: Codestar will automaticly trigger the pipeline when you push to your repos master branch

Architecture

![PipelineAutomation](./AWS-SSO-Pipeline.png)


### Full Automation Pair
If you want full automation for SSO check out https://github.com/DMEvanCT/SSOAutomation 

You can pair both these tools together to get an automated experience inside of AWS SSO. 

Replace for your company
```bash
find ./ -exec sed -i 's/devops@examplecompany.io/yourcompany@examplecompany.io/g' {} \;
find ./ -exec sed -i 's/examplecompany/yourcompanyname/g' {} \;
find ./ -exec sed -i 's/ExampleCompany/YourCompanyName/g' {} \;
```
