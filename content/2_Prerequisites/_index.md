---
title: "Prerequisites"
menuTitle: "Prerequisites"
weight: 20
---

Before attempting to create a stack with the templates, a few prerequisites should be checked to ensure a successful deployment:
1.  Review the key parameters for the inspection and spoke templates to understand what will be deployed based on parameters selection. Reference [**GWLB-in-AWS/Templates**](https://fortinetcloudcse.github.io/GWLB-in-AWS/5_templates/index.html).
2.	An AMI subscription must be active for the FortiGate license type being used in the template.
    * [**Intel BYOL Marketplace Listing**](https://aws.amazon.com/marketplace/pp/prodview-lvfwuztjwe5b2)
    * [**Intel PAYG Marketplace Listing**](https://aws.amazon.com/marketplace/pp/prodview-wory773oau6wq)
    * [**ARM BYOL Marketplace Listing**](https://aws.amazon.com/marketplace/pp/prodview-ccnrlwz74uwgk)
    * [**ARM PAYG Marketplace Listing**](https://aws.amazon.com/marketplace/pp/prodview-ohcnwr7nr2icy)

3.	The solution requires 1 to 2 EIPs per FGT, depending on parameters selected, to be created so ensure the AWS region being used has available capacity.  Reference [**AWS Documentation**](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-resource-limits.html) for more information on EC2 service quotas and how to request increases.

4.	If BYOL licensing is to be used, ensure these licenses have been registered on the support site.

5.   If BYOL licensing is to be used, **create a new S3 bucket in the same region where the template will be deployed.  If the bucket is in a different region than the template deployment, bootstrapping will fail and the FGTs will be inaccessible**.

6.  If BYOL licensing is to be used, upload these licenses to the root directory of the same S3 bucket from the step above.
