Configuration
=============

This guide covers the basic configuration settings for the Yii2-user.

Available configuration options
-------------------------------

- **enableRegistration** Whether registration is enabled. Defaults to **True**.

- **enableGeneratingPassword** Whether password field is not shown on signup
  page and password is generated automatically and sent to user via email.
  Defaults to **False**.

- **enableConfirmation** Whether users have to confirm their accounts by
  clicking confirmation link sent them by email. In order to enable this option
  you have to configure **mail** application component. Defaults to **True**.

- **enableUnconfirmedLogin** Whether users are allowed to sign in without
  activating their accounts. Default to **False**.

- **enablePasswordRecovery** Whether users are allowed to recover their
  passwords. Defaults to **True**.

- **enableEmailReconfirmation** Whether users have to reconfirm their email after
  changing it on settings page. Defaults to **False**.

- **confirmWithin** The time in seconds before a confirmation token becomes invalid. After expiring this time user
  have to request new confirmation token on special page. Defaults to **86400** (24 hours).

- **rememberFor** The time in seconds you want the user will be remembered without asking for credentials. Defaults
  to **1209600** (2 weeks).

- **recoverWithin** The time in seconds before a recovery token becomes invalid. After expiring this time user
  have to request new recovery message. Defaults to **21600** (6 hours).

- **admins** An array of user's usernames who can manage users from admin panel. Defaults to empty array.

- **cost** Cost parameter used by the Blowfish hash algorithm. Defaults to **10**.

- **urlPrefix** The prefix for user module URL. Defaults to **"user"**.

- **urlRules** The rules to be used in URL management.


Configuration example
---------------------

The configuration is done in the application's ``config/web.php`` file.

.. code-block:: php

    <?php return [
        ...
        'modules' => [
            ...
            'user' => [
                'class' => 'dektrium\user\Module',
                'enableUnconfirmedLogin' => true,
                'confirmWithin' => 21600,
                'cost' => 12,
                'admins' => ['admin']
            ],
            ...
        ],
        ...
    ];
