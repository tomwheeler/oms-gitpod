# oms-gitpod

This repository contains files used to configure GitPod for 
the Order Management System (OMS) Reference Application.

This is a work-in-progress, as the web application does not 
currently function correctly when running in GitPod. Also, 
the VSCode customizations appear to be ignored, which is 
perhaps caused by the use of the multi-repo feature in GitPod
(which I suspect can't find the customizations). This is 
more than a nuisance, since it means that new terminal 
sessions won't have the correct environment and therefore 
won't have the `temporal` or `tctl` commands in the `$PATH`. 
Once I get these problems solved, I plan to transfer ownership 
to @temporalio.

Additionally, the application is pretty slow to start up, 
primarily due to the installation of `pnpm` and downloading 
of the Go dependencies happening at launch time. I could 
likely speed that up by doing those steps during the build 
of the Docker image from which the workspace is created 
(though I'd want to fork this from the edu one on which it's 
currently based, since these tasks aren't relevant to our 
training courses).

[![Open in Gitpod](https://gitpod.io/button/open-in-gitpod.svg)](https://gitpod.io/#https://github.com/tomwheeler/oms-gitpod)
