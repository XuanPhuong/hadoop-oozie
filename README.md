## Oozie for Hadoop 2.x

This is an image that applies some changes to the uber profile of oozie/webapp and builds an Oozie distro with the hadoop-2 profile
and Hadoop 2.7.1 libraries.

## Usage

#### Install Oozie sharelib to HDFS

    docker run -ti --rm \ 
    equemuelcompellon/hadoop-oozie oozie-setup.sh sharelib create -fs hdfs://namenode:port

#### Start Ooozie

    docker run -d --name oozie -p 11000:11000 -p 11001:11001 \
    equemuelcompellon/hadoop-oozie oozied.sh run
