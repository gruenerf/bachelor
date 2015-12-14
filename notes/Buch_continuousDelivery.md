Titel: Continuous Delivery
Date: 2011
Verlag: Pearsons Education
Autor: Jez Humble, david farley

Foreword:
Bi-weekly releases now common in fowlers teams.
Foundation for CD is CI. Jedoch reicht CI alleine nicht aus, da Code, welcher nur in die  Mainline integriert ist nocht lange nicht code ist, welcher seinen Zweck in der Production umgebung erfüllt
Der Delivery Prozess fällt zwischen Entwicklern und Operations Team. Ebenso schließt es Tester ein -> daher hohe automatisierung

Preface:
First line agile manifesto: "our highest priority is to satisfy the customer through early and continuous delivery of valuable software."
 -> For successful software the first release is just the beginning of the delivery process
 
#part 1
##1. The Problem of delivering software

Common Problem -> good idea -> how to deliver it to the user afap?
There are a lot of different softwaredevelopment methodologies but most of them only focus on a fragment of the value stream.
Deployment pipeline (build,deploy,test and release)
    commit stage (compile,unit tests, analysis, build installers)
    automated acceptance testing
    automated capacity testing
    manual testing (showcases, exploratory testing)
    release
The deployment pipeline has its foundations in the process of CI and is in essence the principle of Ci taken to its logical conclusion
Aim of the pipeline: making all steps visible/improves feedback (resolving of problems as early as possible)/fully automated release
Problems: 

Why automated deployment?
    If not fully automated errors will occur each timer they´e performed
    it´ repeatable
    manual deployment needs a lot of manual documentation -> time consuming task
    automated deployment encourages collaboration
    Testing a manual deployment is to do it -> time consuming and expensive
    high auditability
