Repo Manifest for OpenEmbedded Bitbake Layers
=============================================

Manifest project for using Google Repo to manage a bunch of OpenEmbedded bitbake
layers.

Note that this does not include the Yocto Project's Poky repository. Instead,
the import pieces that go into the poky repository are included from their
upstream git repositories directly (e.g. oe-core, bitbake, etc).

This repo manifest exists to make it easier to submit changes to the base
repositories as required by the poky documentation.

Getting Started
---------------

1.  Install Google's Repo command.

    Download the Repo script:

        $ curl http://commondatastorage.googleapis.com/git-repo-downloads/repo > repo
        $ chmod a+x repo
        $ sudo mv repo /usr/local/bin/

2.  Initialize a Repo client.

    Create an empty directory to hold your working files:

        $ cd ${HOME}/${WORK_DIR}
        $ mkdir oe-core
        $ cd oe-core

    **NOTE**: Use whatever you want for `${WORK_DIR}` and/or `oe-core`, just
    adjust what follows accordingly.

    Tell Repo where to find the manifest:

        $ repo init -u git://github.com/openavr/manifest-oe -b main

    A successful initialization will end with a message stating that Repo is
    initialized in your working directory. Your client directory should now
    contain a `.repo` directory where files such as the manifest will be kept.

3.  Fetch all the repositories:

        $ repo sync
