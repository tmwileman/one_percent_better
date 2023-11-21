# Effective Cost Analyses

I'm currently responsible for putting together a project's cost analysis. This is the first one I've done and while I have an idea of the basic elements, I am not sure what makes a cost analysis truly effective. 

# Document's Purpose
This is a decision aid. Should management greenlight further development on this project based on the expected costs and benefits. If I were in a position to make a decision based on this document, high level questions I'd want answered are:

- **What is the problem?** - What is the current situation? Why is it bad? **How** bad is it (quantify)? This needs to provide plenty of context but be suscinct at the same time. I want who ever is reading this to **feel** the pain and want to help us solve the issue. 
- **What are possible solutions?** - There's never just one way to solve a problem. Here, I want to convey that we've thought through all possible soluions. This builds trust in my eventual recommendation. I want to clearly lay out the pros and cons of each solution. 
- **How much does each solution cost?** - Bottom line, what is the expected cost of each solution. Both from a high level (total cost) and low level (cost of solution components). This should be straightforward. You've already laid out the solutions and the pieces that make them up. Now just tell who ever is reading how much they can expect to pay over some relevant period of time. 
- **Benefits of solution** - How does the proposed solution fix the problem. Ideally (I can't think an instance where this wouldn't be the case) there is cost savings component. Possible benefits include expected revenue from customers, estimated hours of work saved (translated into dollars), risk reductions, or efficiency gians. Again, translating all to dollars is almost certainly ideal. 
- **Possible risks** - How might the analysis be wrong and what are mitigating steps we can take to identify and counteract those risks. Again, I view this as more of an element that builds trust in the thoroughness of the analysis. "You should trust me because I've thought of all these things and have plans for all these contingencies."

# What I Need to Find Out
My analysis has to do with cloud computing costs. I've spun up personal computing instances on AWS and other cloud providers for small data science projects but haven't done so for large, production level projects. 

Thus far my research into how much this project might cost is based on publically available pricing sheets. I'm simply choosing the GPU-based instance that meets my expected requirements and extrapolating the costs out for a year based on the hourly price. 

I have a feeling this is incomplete but unsure how to improve. For example, do I need additional compute elements like an API gateway? Is this price subject to change over the course of the year or could it change? Can we get a discount on a second instance if we need it? What are some commone issues others more familiar with this work would recommend

# Insights Gained From Research
- [Investopedia](https://www.investopedia.com/terms/c/cost-benefitanalysis.asp)
    - More complex cost-benefit analysis may incorporate sensitivity analysis or discounting of cashflows
    - Sensitivity Analysis - How slight changes in estimates may impact outcomes.
    - Discounting Cashflows - Calculate the present value of expected future cash flows using a discount rate. For example, $100 invested today in a savings scheme with a 10% interest rate will grow to $110. In other words, $110, which is the future value (FV), when discounted by the rate of 10%, is worth $100 (present value) as of today. DR = ( FV ÷ PV ) 1/n - 1.
- [DEV](https://dev.to/aws-builders/privategpt-and-aws-ec2-a-beginners-guide-to-ai-experimentation-2npm)
    - Start by setting up the AWS EC2 instance:
    - Choose OS
    - Select instance type
    - Storage configuration - Any additional storage needed for model
    - Security Group Configuration - Create rules on who can/can't access (IP whitelisting if you're setting up private instance). Not sure this is required for my purpose or if it is how I should configure.
    - Use AWS Session Manager to interact with instances.
- [Reddit](https://www.reddit.com/r/aws/comments/12ibgmp/how_good_is_aws_for_opensource_llms/)
    - Lambda doesn't support GPUs and limited to 10 GB of RAM
    - SageMaker is limited to a single instance
    - EKS could be used to spin up multiple GPU nodes
    - [SageMaker can be used for multinode training](https://medium.com/@emilywebber/how-i-trained-10tb-for-stable-diffusion-on-sagemaker-39dcea49ce32)
- [ChatGPT]
    - Hosting a Large Language Model (LLM) on AWS and accessing it via an API involves several steps, including setting up an AWS environment, deploying the model, and creating an API for access. Here's a high-level overview of how you can do this:

    1. **Choose the Right AWS Service**:
    - AWS offers various services for hosting machine learning models. The most suitable for hosting an LLM might be Amazon SageMaker, which allows you to deploy machine learning models on fully managed instances.

    2. **Prepare the LLM**:
    - If you have a pre-trained LLM, ensure it's in a format compatible with AWS services. If not, you might need to train or fine-tune a model using tools like SageMaker.

    3. **Set Up Amazon SageMaker**:
    - Create a SageMaker instance in the AWS Management Console.
    - Upload your model to Amazon S3, a cloud storage service, which can then be accessed by SageMaker.

    4. **Deploy the Model**:
    - Use SageMaker to deploy your model to a real-time endpoint. This process involves creating a model, configuring an endpoint, and deploying the model to the endpoint.

    5. **Create an API**:
    - Use Amazon API Gateway to create an API that will interact with your SageMaker endpoint.
    - Define the API resources, methods, and integration requests to connect the API Gateway to the SageMaker endpoint.

    6. **Set Up Authentication and Access**:
    - Configure authentication and access control for your API. You can use AWS Identity and Access Management (IAM) to manage access to your API.

    7. **Test the API**:
    - Once your API is set up, test it to ensure it's correctly receiving requests and the SageMaker endpoint is responding as expected.

    8. **Monitoring and Management**:
    - Use Amazon CloudWatch to monitor the performance of your API and the SageMaker endpoint.
    - Set up logging and alarms for tracking and notification purposes.

    9. **Documentation and SDKs**:
    - Document the API for developers who will use it.
    - Optionally, generate SDKs in different languages for easy integration with various platforms.

    10. **Cost Management**:
    - Be aware of the costs associated with AWS services like SageMaker, API Gateway, and S3. Use AWS Cost Management tools to monitor and optimize expenses.

    Remember, working with AWS and deploying machine learning models at scale requires a good understanding of cloud computing, AWS services, and machine learning deployment best practices. If you're new to these areas, you might want to explore AWS tutorials, documentation, or consider getting assistance from someone with expertise in AWS and machine learning.

# Takeaways
 - I need to do this once on my own to see how it all fits together. It seems like I can just use the EC2 instance or SageMaker for hosting and then add an API Gateway that points to my end point.

 - My analysis is on the right track but I need to add the following elements:
    - Graphic of proposed architecture
    - Break down of expected cost of each component in the architecture (I only have EC2 instance now)
    - Find a way to quantify the problem
        - How many times is the instance I'm concerned about occuring
        - How much money might that represent
    - Define my scope to be either only the cost of inference or the cost of inference and the cost of retraining. Leaning toward the latter.

- The keys to a good cost analysis are:
    - Trust in the underlaying analysis
        - Explored all possible solutions
        - Problem is quantified and expressed in monetary terms
        - Benefits are realistic and also financially quantified
    - Simple message
        - Do or do not do this based on these findings