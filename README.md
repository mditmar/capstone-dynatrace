# Solutions Engineering Capstone

Thank you for your interest in joining the Solutions Engineering team at Dynatrace. The next step is to set up and demo an environment of your choosing, instrumented with the Dynatrace 3rd-generation platform. The goal of this capstone is to showcase your technical skills, your fluency with the modern Grail-backed, AI-driven Dynatrace platform, and your ability to present its value to multiple business units in a single presentation.

See below for instructions and expectations of this demo and please reach out to the hiring manager (mike.ditmar@dynatrace.com) with any questions.

---
### Setup

**1. Sign up for a free Dynatrace SaaS trial**
    - https://www.dynatrace.com/signup/

**2. Deploy OneAgent to your environment**
  - [Linux](https://docs.dynatrace.com/docs/ingest-from/dynatrace-oneagent/installation-and-operation/linux/installation/install-oneagent-on-linux)
  - [Windows](https://docs.dynatrace.com/docs/ingest-from/dynatrace-oneagent/installation-and-operation/windows/installation/install-oneagent-on-windows)
  - [Kubernetes / OpenShift - Helm](https://docs.dynatrace.com/docs/ingest-from/setup-on-k8s/deployment/full-stack-observability)
  - [Kubernetes / OpenShift - Manifest Deployment](https://docs.dynatrace.com/docs/shortlink/installation-k8s-cloud-native-fs#manifest)


**3. Deploy a Web Application**
    
  Set up a demo application in your environment.

  Requirements of the demo application:
  - Front end web server (for browser RUM injection) 
  - Code level calls more advanced than a "hello world" or health check 
    -  Check [Dynatrace's list of supported technologies](https://docs.dynatrace.com/docs/ingest-from/technology-support) for technology compatibility
  - Application logs are generated and available (stdout by default)
  - A Database component 
  - The application must be capable of generating errors/ crashes/ outages

    Any application that meets the requirements above will work. Here are a couple of recommended sample apps:

    - [Online Boutique](https://github.com/GoogleCloudPlatform/microservices-demo)
    - [EasyTrade](https://github.com/Dynatrace/easytrade)
    - Any custom application you've worked with or built that meets the requirements above

---
### Demo Requirements

Required capabilities to demonstrate

Each capability below describes WHAT to demonstrate, with links to documentation and demo examples. There's no single right way to do these in Dynatrace — the platform offers multiple paths, and you should pick what fits your demo. The links are meant to be instructional and for starting points, not prescriptions.

**1. Infrastructure**

Demonstrate the health and performance of the infrastructure that makes up your environment.
   
- **Infrastructure and Operations**
  - [Documentation](https://www.dynatrace.com/hub/detail/infrastructure-operations/)
  - [Video](https://docs.dynatrace.com/docs/manage/segments)
   
- ***Kubernetes (if applicable)***
  - [Documentation](https://www.dynatrace.com/hub/detail/kubernetes-1/)
  - [Video](https://www.youtube.com/watch?v=gQcaF4Dm7c0&list=PLqt2rd0eew1aHqfD-XRNVaIAiN-QxkPK6&index=9)

**2. Services**

Demonstrate the real-time monitoring of service health and performance across your Application environment.
  
  - [Documentation](https://docs.dynatrace.com/docs/observe/application-observability/services/services-app)
  - [Video](https://www.youtube.com/watch?v=35rzyxQZCpY)   

**3. Traces**

One of the core tenants of Observability, demonstrate distributed traces from your Application to analyze where time is spent, service interaction and error inspection.
  - [Documentation](https://www.dynatrace.com/hub/detail/distributed-tracing/)
  - [Video](https://www.youtube.com/watch?v=O4zWlwJ4hsA&list=PLqt2rd0eew1aHqfD-XRNVaIAiN-QxkPK6&index=10)
  
**4. Logs**

Ensure that your Host, Process and Application logs are being ingested into Dynatrace and demonstrate logs in context of your traces as well as querying logs.
  
- **Logs in context of traces**
  - [Logs ingestion - Documentation](https://docs.dynatrace.com/docs/analyze-explore-automate/logs/lma-log-ingestion)
  - [Connecting Logs to Traces - Documentation](https://docs.dynatrace.com/docs/analyze-explore-automate/logs/lma-log-enrichment)
    
- **Querying Logs**
  - [Logs App - Documentation](https://www.dynatrace.com/hub/detail/logs/)
  - [Logs App - Video](https://www.youtube.com/watch?v=cwF-Md_oFHM&list=PLqt2rd0eew1aHqfD-XRNVaIAiN-QxkPK6&index=11)


**5. Frontend / Real User Monitoring**

Your demo application should contain a Web frontend where user sessions and activity can be tracked and correlated to the backend services. Demonstrate 
    
**6. Dashboards**

**7. AI-driven analysis**

Demonstrate AI-driven insights using [Dynatrace Intelligence](https://docs.dynatrace.com/docs/dynatrace-intelligence). It is recommended to have your demo Application experience a failure, crash, errors so that Dynatrace's Anomaly Detection will automatically detect this behavior and generate a Problem.
    - [Problems App](https://www.youtube.com/watch?v=Tud2K3zyync&list=PLqt2rd0eew1aHqfD-XRNVaIAiN-QxkPK6&index=6) for analyzing issues within your environment. 
    - [Dynatrace Assist](https://docs.dynatrace.com/docs/dynatrace-intelligence/agentic-and-generative-ai/chat-with-dynatrace-assist) generating DQL in a Notebook
    - for guided analysis
    - Predictive forecast or anomaly detection on a chart

**8. Notebooks and DQL**

Build at least one [Notebook](https://docs.dynatrace.com/docs/analyze-explore-automate/dashboards-and-notebooks/notebooks) that includes at least one [DQL](https://docs.dynatrace.com/docs/platform/grail/dynatrace-query-language) query you wrote (or that Davis CoPilot generated and you refined).

---
### Strongly Recommended

These are not required, but it is strongly encouraged that you configure some of these. Make sure you call these out during your demo if you set them up!

**AI Coding Assistants**
- Use AI Coding Assistants (GitHub Copilot, Claude Code, etc.) to Configure, Troubleshoot and Interact with your Dynatrace Tenant
- The use of Coding Assistants is very helpful to generate queries, build dashboards, configure or troubleshoot configurations, etc.
  - [dtctl](https://github.com/dynatrace-oss/dtctl#dtctl) CLI for the Dynatrace platform
  - [AI Agent Skills for Coding Agents](https://github.com/dynatrace-oss/dtctl#ai-agent-skills) teaches AI coding assistants how to use dtctl
  - [Dynatrace Domain Skills](https://github.com/dynatrace-oss/dtctl#dynatrace-domain-skills) For deeper Dynatrace domain knowledge for your coding assistants

**Optional / Explore**

These are not required, but other areas that you can choose to configure. Make sure you call these out during your demo if you set them up!

- [Site Reliability Guardian](https://docs.dynatrace.com/docs/deliver/site-reliability-guardian) for release validation
- [Cloud account integration](https://docs.dynatrace.com/docs/observe/infrastructure-observability/cloud-platform-monitoring) (AWS, Azure, GCP)
- [RUM Session Properties](https://docs.dynatrace.com/docs/observe/digital-experience/web-applications/additional-configuration/define-user-action-and-session-properties)
- [Dynatrace Terraform Provider](https://registry.terraform.io/providers/dynatrace-oss/dynatrace/latest) for at least one configuration

---
### Presentation Notes and Tips

Your presentation should highlight your technical aptitude by demonstrating the core concepts and feature functionality of the platform. However, the primary focus of your presentation will be to demonstrate the value of the Dynatrace observability platform for the given audience. For the purposes of this demo the Dynatrace Solutions Engineering team will be role-playing as stakeholders of a prospect in the roles of:
- Observability Teams
- Application Owners
- Application Developers
- SRE Teams
- IT Operations

Come prepared with these roles in mind and tailor your presentation to demonstrate how these personas will drive better business outcomes with the Dynatrace platform (drive revenue, reduce costs, improve efficiency, release faster, etc.) Additionally, be prepared to field live questions from these stakeholders about the Dynatrace platform from their specific lens.

- Get to know your audience. Understand the background of your audience to tailor the narrative and depth of your demo.
- Highlight just the key features. Focus on the most important technical features and how they impact the user, but avoid a "feature demo".
- Articulate the practical application of the platform. Explain how the technical features solve real-world problems for your audience.
- Be prepared for questions & interruptions from your audience
- Try to maintain engagement. Keep the audience engaged with interaction and encourage questions throughout the demo.
        
Additional links for that may be helpful for your preparation:
- [Dynatrace YouTube Channel](https://www.youtube.com/@dynatrace)
- [Dynatrace LinkedIn](https://www.linkedin.com/company/dynatrace/posts/?feedView=all)
- [Dynatrace Playground SaaS Environment](https://wkf10640.apps.dynatrace.com/) — login required; uses the email associated with your Dynatrace account (created when you sign up for a trial)
- [Dynatrace Blog](https://www.dynatrace.com/news/blog/)
- [Getting started with Dynatrace](https://docs.dynatrace.com/docs/discover-dynatrace/get-started)
- [Product News](https://www.dynatrace.com/news/blog/)


Have fun!

---

*Last reviewed: August 2026 — content reflects the Dynatrace 3rd-generation platform.*
