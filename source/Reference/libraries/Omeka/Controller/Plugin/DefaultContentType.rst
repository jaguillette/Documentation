------------------------------------------
Omeka_Controller_Plugin_DefaultContentType
------------------------------------------

Package: :doc:`Controller\\Plugin </Reference/packages/Controller/Plugin/index>`

.. php:class:: Omeka_Controller_Plugin_DefaultContentType

extends :php:class:`Zend_Controller_Plugin_Abstract`

    This controller plugin sets the default Content-Type header when one hasn't
    been set at the end of the controller processing.

    This has to be done here because Zend allows header duplication, the output contexts don't overwrite headers of the same name, and some servers
    (FastCGI) choke when they see two Content-Type headers.

    .. php:method:: dispatchLoopShutdown()

        Add a default Content-Type to the response if none is already set.
