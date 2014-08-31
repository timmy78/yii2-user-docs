Social auth
===========

Yii2-user supports authentication using social networks accounts. It allows to
connect social accounts to user account and use them to log in.

Getting started
---------------

To get started you need to setup auth client collection application component:

.. code-block:: php

    <?php
    return [
        ...
        'components' => [
            ...
            'authClientCollection' => [
                'class' => 'yii\authclient\Collection',
                'clients' => [
                    'google' => [
                        'class' => 'yii\authclient\clients\GoogleOpenId'
                    ],
                    'facebook' => [
                        'class' => 'yii\authclient\clients\Facebook',
                        'clientId' => 'facebook_client_id',
                        'clientSecret' => 'facebook_client_secret',
                    ],
                ],
            ],
            ...
        ],
        ...
    ];

How it works
------------

When you are going to log in you can click social network icon. If you have
already logged in using that account you will be logged in. Otherwise you will
be shown simple sign up form with two field (username and email).

After you logged in you can go to accounts settings page and connect new account
or disconnect already connected accounts.
