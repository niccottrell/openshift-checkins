# Red Hat OpenShift Checkins App

## Getting Started

Clone the source and build the app. You'll need [Java](http://www.java.com/en/download/manual.jsp) and [Maven](http://maven.apache.org) in order to build. It probably wouldn't hurt to have download and install [MongoDB](https://www.mongodb.com/download-center) either.

    $ git clone http://github.com/niccottrell/openshift-checkins.git
    $ cd openshift-checkins
    $ mvn package

To deploy the app you'll need an [OpenShift](https://openshift.redhat.com/app/) account and install the tools:

    $ gem install rhc
    
Now you can deploy the ``checkins.war`` file to OpenShift. Once deployed, test it like so:

    $ curl -X POST -d "comment=hello&x=1&y=1" http://appurl.rhcloud.com/checkin

For a more in-depth guide, refer to the [OpenShift Quickstart](https://docs.mongodb.com/ecosystem/platforms/red-hat-openshift/) guide at [mongodb.org](http://www.mongodb.com).
