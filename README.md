# Solutions Engineering Capstone

Thank you for your interest in joining the Solutions Engineering team at Dynatrace. The next step is to set up and demo an environment of your choosing, instrumented with the Dynatrace 3rd-generation platform. The goal of this capstone is to showcase your technical skills, your fluency with the modern Grail-backed, AI-driven Dynatrace platform, and your ability to present its value to multiple business units in a single presentation.

See below for further instructions and expectations of this demo and reach out to your hiring manager or kyle.harrington@dynatrace.com with any questions.
    
If you are planning on using a Dynatrace Managed install for this demo, please see the [Dynatrace Managed Capstone](/dt-managed/dt-managed-capstone.md) for instructions

---

1. Sign up for a free Dynatrace SaaS trial
    - https://www.dynatrace.com/signup/

1. Deploy OneAgent to your environment
    - [Linux](https://docs.dynatrace.com/docs/ingest-from/dynatrace-oneagent/installation-and-operation/linux/installation/install-oneagent-on-linux)
    - [Windows](https://docs.dynatrace.com/docs/ingest-from/dynatrace-oneagent/installation-and-operation/windows/installation/install-oneagent-on-windows)
    - [Kubernetes / OpenShift - Helm](https://docs.dynatrace.com/docs/ingest-from/setup-on-k8s/deployment/full-stack-observability)
    - [Kubernetes / OpenShift - Manifest Deployment](https://docs.dynatrace.com/docs/shortlink/installation-k8s-cloud-native-fs#manifest)

    For cloud-native applications, [OpenTelemetry OTLP](https://docs.dynatrace.com/docs/ingest-from/opentelemetry) is also a valid ingest path and can be used in place of, or alongside, OneAgent.

1. Deploy a Web Application
    
    Set up a demo application in your environment.

    Requirements of the demo application 
    - Front end web server (for browser RUM injection) 
    - Code level calls more advanced than a "hello world" or health check 
      -  Check [Dynatrace's list of supported technologies](https://docs.dynatrace.com/docs/ingest-from/technology-support) for technology compatibility
    - Application logs are generated and available (stdout by default)
    - A Database component 
    - The application must be capable of generating errors/ crashes/ outages

    Any application that meets the requirements above will work. Recommended sample apps (in suggested order):

    - [Astronomy Shop](https://opentelemetry.io/docs/demo/kubernetes-deployment/)
    - [Online Boutique](https://github.com/GoogleCloudPlatform/microservices-demo)
    - [EasyTrade](https://github.com/Dynatrace/easytrade)
    - Any custom application you've worked with or built that meets the requirements above


1. Required capabilities to demonstrate

    Each capability below describes WHAT to demonstrate, with linked options for HOW. There's no single right way to do these in Dynatrace — the platform offers multiple paths, and you should pick what fits your demo. The linked docs are starting points, not prescriptions.

    **4.1 Data organization & filtering**

    Demonstrate how you organize and filter data in your environment. Options include:
    - [Segments](https://docs.dynatrace.com/docs/manage/segments) (query-time filter conditions on Grail)
    - [Grail buckets](https://docs.dynatrace.com/docs/platform/grail/organize-data) for data partitioning and retention
    - [IAM data-access policies on Grail](https://docs.dynatrace.com/docs/platform/grail/organize-data/assign-permissions-in-grail)
    - [OneAgent host groups](https://docs.dynatrace.com/docs/observe/infrastructure-observability/hosts/configuration/organize-your-environment-using-host-groups)
    - [OneAgent host tagging](https://docs.dynatrace.com/docs/manage/tags-and-metadata/setup/how-to-define-tags)

    **4.2 Alerting & notification routing**

    Demonstrate how problems and events route to the right teams or channels. Options include:
    - [Workflows](https://docs.dynatrace.com/docs/analyze-explore-automate/workflows) for event-driven routing and automation
    - Workflow integrations with Slack, Microsoft Teams, ServiceNow, PagerDuty, or custom notification endpoints

    **4.3 Telemetry enrichment & tagging**

    Demonstrate how you enrich telemetry with ownership, environment, or business context. Options include:
    - [OneAgent host tagging](https://docs.dynatrace.com/docs/manage/tags-and-metadata/setup/how-to-define-tags) at deployment time
    - [OpenPipeline](https://docs.dynatrace.com/docs/platform/openpipeline) processors for in-flight enrichment
    - Extension enrichment attributes (security context, product, cost center)
    - Kubernetes labels via the Dynatrace Operator

    **4.4 Logs, metrics, and traces**

    - [Logs ingestion](https://docs.dynatrace.com/docs/analyze-explore-automate/logs/lma-log-ingestion) (OneAgent, OpenPipeline, OTLP, Cribl, or custom)
    - [Metric ingestion](https://docs.dynatrace.com/docs/analyze-explore-automate/metrics) (OneAgent metric API, Prometheus, OTLP, extensions)
    - [Trace ingestion](https://docs.dynatrace.com/docs/observe/application-observability/distributed-tracing/ingest-traces) (OneAgent auto-instrumentation, OTLP)

    **4.5 Real User Monitoring**

    - [Browser monitoring check](https://docs.dynatrace.com/docs/observe/digital-experience/synthetic-monitoring/browser-monitors/create-a-single-url-browser-monitor) for your web app
    - [Session Replay](https://docs.dynatrace.com/docs/observe/digital-experience/session-replay/enable-session-replay-web)
    - [Conversion goals](https://docs.dynatrace.com/docs/observe/digital-experience/web-applications/analyze-and-use/define-conversion-goals) for the web app

    **4.6 AI-driven analysis**

    Demonstrate at least one AI-driven insight using [Davis](https://docs.dynatrace.com/docs/dynatrace-intelligence). Options include:
    - Davis problem root-cause walkthrough
    - [Davis CoPilot](https://docs.dynatrace.com/docs/dynatrace-intelligence/agentic-and-generative-ai/agentic-and-generative-ai-getting-started) generating DQL in a Notebook
    - [Dynatrace Assist](https://docs.dynatrace.com/docs/dynatrace-intelligence/agentic-and-generative-ai/chat-with-dynatrace-assist) for guided analysis
    - Predictive forecast or anomaly detection on a chart

    **4.7 Notebooks and DQL**

    Build at least one [Notebook](https://docs.dynatrace.com/docs/analyze-explore-automate/dashboards-and-notebooks/notebooks) that includes at least one [DQL](https://docs.dynatrace.com/docs/platform/grail/dynatrace-query-language) query you wrote (or that Davis CoPilot generated and you refined).


1. Strongly recommended

    These are not required, but it is strongly encouraged that you configure some of these. Make sure you call these out during your demo if you set them up!

    - [OpenPipeline](https://docs.dynatrace.com/docs/platform/openpipeline) — ingest transformation and enrichment
    - [BizEvents / Business Analytics](https://docs.dynatrace.com/docs/observe/business-observability/bo-events-capturing)
    - [Log Events](https://docs.dynatrace.com/docs/analyze-explore-automate/logs/lma-log-processing/lma-log-events)
    - [OpenTelemetry OTLP ingest](https://docs.dynatrace.com/docs/ingest-from/opentelemetry) (if you didn't already exercise OTLP in §4.4)
    - [Site Reliability Guardian](https://docs.dynatrace.com/docs/deliver/site-reliability-guardian) for release validation
    - [Live Debugger](https://docs.dynatrace.com/docs/observe/application-observability/live-debugger)
    - [Runtime Vulnerability Analytics](https://docs.dynatrace.com/docs/secure/application-security/vulnerability-analytics)
    - [Kubernetes Security Posture Management](https://docs.dynatrace.com/docs/ingest-from/setup-on-k8s/deployment/security-posture-management)
    - [Cloud account integration](https://docs.dynatrace.com/docs/observe/infrastructure-observability/cloud-platform-monitoring) (AWS, Azure, GCP)
    - [RUM Session Properties](https://docs.dynatrace.com/docs/observe/digital-experience/web-applications/additional-configuration/define-user-action-and-session-properties)
    - [Dynatrace Terraform Provider](https://registry.terraform.io/providers/dynatrace-oss/dynatrace/latest) for at least one configuration

    Feel free to review the full Dynatrace product documentation on [Getting started with Dynatrace](https://docs.dynatrace.com/docs/discover-dynatrace/get-started) and [Product News](https://www.dynatrace.com/news/blog/) pages and come up with your own integration ideas for your demo.


1. Optional / explore

    These aren't expected for the capstone, but they're great differentiators if you want to show platform breadth or AI fluency.

    - [Dynatrace MCP Server](https://docs.dynatrace.com/docs/dynatrace-intelligence/dynatrace-mcp) + [Dynatrace for AI agent skills](https://github.com/Dynatrace/dynatrace-for-ai) — connect Claude Code, Cursor, Copilot, or other AI coding agents to your live tenant for real-time platform context
    - [OneAgent SDK](https://docs.dynatrace.com/docs/ingest-from/extend-dynatrace/extend-tracing/oneagent-sdk) for non-native language instrumentation
    - [Python OneAgent auto-instrumentation](https://github.com/dynatrace-oss/OneAgent-SDK-Python-AutoInstrumentation)
    - [Private ActiveGate synthetic location](https://docs.dynatrace.com/docs/observe/digital-experience/synthetic-monitoring/private-synthetic-locations/create-a-private-synthetic-location)
    - [Events API](https://docs.dynatrace.com/docs/dynatrace-api/environment-api/events-v2/post-event) for injecting entity events
    - Custom [Strato](https://developer.dynatrace.com/design/about-strato-design-system/) app on [AppEngine](https://docs.dynatrace.com/docs/platform/appengine) — see the [5-minute quickstart](https://developer.dynatrace.com/quickstart/first-app-in-5-minutes/)


1. Presentation Overview

    Your presentation should highlight your technical aptitude by demonstrating the core concepts and feature functionality of the platform. However, the primary focus of your presentation will be to demonstrate the value of the data provided by Dynatrace to multiple business units, teams, and stakeholders for any given organization. For the purposes of this demo the Dynatrace Solutions Engineering team will be role-playing as stakeholders of a prospect in the roles of:

    - C-Suite Leadership
    - Technology Operations
    - Software Development
    - DevOps
    - Site Reliability Engineer
    - Infrastructure Support
    - Business Analytics & Intelligence
    - etc

    Come prepared with these roles in mind and tailor your presentation to demonstrate how each of these teams' day-to-day jobs could be different and drive better business outcomes with the Dynatrace platform. Additionally, be prepared to field live questions from these stakeholders about the Dynatrace platform from their specific lens.

1. Presentation requirements: 

    Below is a list of the required features, applications and/or functionality of the Dynatrace platform which need to be incorporated into your demo. 

    Dynatrace Apps
    - [Problems App](https://www.dynatrace.com/hub/detail/problems/)
    - [Infrastructure and Operations](https://www.dynatrace.com/hub/detail/infrastructure-operations)
    - [Logs App](https://www.dynatrace.com/hub/detail/logs/)
    - [Traces App](https://www.dynatrace.com/hub/detail/distributed-tracing)
    - [Services App](https://www.dynatrace.com/hub/detail/services-1/)
    - [Kubernetes App](https://www.dynatrace.com/hub/detail/kubernetes-1) (if you leveraged Kubernetes)
    - [Notebooks App](https://www.dynatrace.com/hub/detail/notebooks/)
    - [Dashboards App](https://www.dynatrace.com/hub/detail/dashboards/)
    - [Dynatrace Assist](https://www.dynatrace.com/hub/detail/ask-davis-copilot/)
    - [Smartscape](https://docs.dynatrace.com/docs/analyze-explore-automate/smartscape)

    Features
    - At least one [DQL](https://docs.dynatrace.com/docs/platform/grail/dynatrace-query-language) query you wrote (or that Davis CoPilot generated and you refined)
    - At least one [Workflow](https://docs.dynatrace.com/docs/analyze-explore-automate/workflows) that routes an event, sends a notification, or triggers automation
    - At least one Davis-driven insight — a Davis problem root-cause, a [Davis CoPilot](https://docs.dynatrace.com/docs/dynatrace-intelligence/agentic-and-generative-ai/agentic-and-generative-ai-getting-started) interaction, [Dynatrace Assist](https://docs.dynatrace.com/docs/dynatrace-intelligence/agentic-and-generative-ai/chat-with-dynatrace-assist), a predictive forecast, or anomaly detection
    - The configured [browser monitoring check](https://docs.dynatrace.com/docs/observe/digital-experience/synthetic-monitoring/browser-monitors/create-a-single-url-browser-monitor) for your web application
    - The configured [Session Replay](https://docs.dynatrace.com/docs/observe/digital-experience/session-replay/enable-session-replay-web) sessions
    - The configured [conversion goals](https://docs.dynatrace.com/docs/observe/digital-experience/web-applications/analyze-and-use/define-conversion-goals) for your web application

    Demo Expectations
    - All of the above "Dynatrace apps" and "features" are incorporated into your demo
    - Present a problem card generated in your environment and the related application, user, service, and business impact
    - Build a dashboard that showcases your environment and its data
    - Build at least one Notebook with at least one DQL query
    - Demonstrate at least one AI-driven insight
    - Walk through the application service flow you've instrumented with OneAgent from front-end (Real Users) to the backend (database calls)
    - Highlight the value of the data provided by the Dynatrace platform to your audience
    - Incorporate how you would benefit from the Dynatrace platform & data you are presenting in your current or previous role(s)

    Tips for success:

    The overarching theme of your presentation should hinge on the business value these requirements provide to your audience. Focus on business value, highlighting how the Dynatrace platform can drive revenue, reduce costs, or improve efficiency.

    - Get to know your audience. Understand the background of your audience to tailor the narrative and depth of your demo.
    - Highlight just the key features. Focus on the most important technical features and how they work, but avoid a "feature demo" 
    - Articulate the practical application of the platform. Explain how the technical features solve real-world problems for your audience.
    - Be prepared for questions & interruptions from your audience
    - Try to maintain engagement. Keep the audience engaged with interaction and encourage questions throughout the demo.

        
    If you need additional ideas for demos, talking points or general knowledge take a look at:
    - [Dynatrace YouTube Channel](https://www.youtube.com/@dynatrace)
    - [Dynatrace LinkedIn](https://www.linkedin.com/company/dynatrace/posts/?feedView=all)
    - [Dynatrace Playground SaaS Environment](https://wkf10640.apps.dynatrace.com/) — login required; uses the email associated with your Dynatrace account (created when you sign up for a trial)
    - [Dynatrace Blog](https://www.dynatrace.com/news/blog/)


    Additional Notes:
    - Please ensure that you have enabled [Real User Monitoring (RUM)](https://docs.dynatrace.com/docs/observe/digital-experience/web-applications/initial-setup/configure-dynatrace-real-user-monitoring-to-capture-xhr-actions) for your web app
    - Have fun!

---

*Last reviewed: May 2026 — content reflects the Dynatrace 3rd-generation platform.*