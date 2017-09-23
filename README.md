# Proprietary for shamu to build Lineage OS #

# How To
---------------

To initialize your local repository, use this command:

        croot
        cd vendor
        mkdir motorola
        cd motorola
        git init
        git config core.sparseCheckout true
        nano .git/info/sparse-checkout

Input the content in sparse-checkout and ctrl+x to save:

        /shamu/*

Next make sure core.sparseCheckout is true:

        git config --list

Pull from TheMuppets and my git, and then cherry-pick my commits:

        git remote add origin https://github.com/TheMuppets/proprietary_vendor_motorola.git
        git pull origin cm-14.1 --depth=1
        git remote add motoxpro https://github.com/totalatot/proprietary_vendor_motorola.git
        git fetch motoxpro master:motoxpro
	git log motoxpro
	git cherry-pick commit1
	git cherry-pick commit2

Proprietary is done. Start to build you Lineage OS and enjoy.
