.. _reference-linux-fedora-centos-post_instalacion_fedora_kde:

###########################
Post instalación Fedora KDE
###########################

**Fedora 27 KDE**

:ref:`reference-linux-fedora-centos-post_instalacion_fedora`

Desinstalar
***********

.. code-block:: bash

    dnf remove -y \
        akregator \
        amarok \
        calligra* \
        kget \
        kmahjongg \
        kmines \
        knode \
        konqueror \
        kpat \
        ktorrent \
        kwrite

Programas básicos
*****************

.. code-block:: bash

    dnf -y install \
        ffmpegthumbs \
        gvfs \
        kate \
        keepassxc \
        libreoffice \
        setroubleshoot \
        transmission-qt

* ``ffmpegthumbs`` Previews para los videos en Dolphin, se ha de activar igual que las imágenes.
* ``gvfs`` En Atom y VSCode, sin ``gvfs`` no moverá los archivos a la papelera cuando se quieran borrar.

KDEConnect
**********

.. code-block:: bash

    sudo firewall-cmd --zone=public --permanent --add-port=1714-1764/tcp
    sudo firewall-cmd --zone=public --permanent --add-port=1714-1764/udp
    sudo systemctl restart firewalld.service
