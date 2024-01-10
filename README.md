# sample.wsadmin.websphere-traditional
WebSphere Application Server traditional wsadmin scripts:

- [deployOidc.py](https://github.com/WASdev/sample.wsadmin.websphere-traditional/tree/master#deployoidcpy)
- [updateAuthAlias.py](https://github.com/WASdev/sample.wsadmin.websphere-traditional/tree/master#updateauthaliaspy)

## Scripts provided


### deployOidc.py
[deployOidc.py](https://github.com/WASdev/sample.wsadmin.websphere-traditional/blob/master/deployOidc.py) installs the WebSphere OIDC TAI EAR, `WebSphereOIDCRP.ear`, as an admin app called `WebSphereOIDCRP_Admin`.
If you intend to protect the admin console on the deployment manager with the OIDC TAI, the OIDC EAR must be deployed as an admin app.

To install the OIDC EAR as an admin application on your system, run the following command:

```
wsadmin -f deployOidc.py install
```

The `deployOidc.py` can also be used to uninstall the `WebSphereOIDCRP_Admin` application.

You can find steps to protect the admin console with OIDC at [How to protect the WebSphere admin console by using OIDC](https://www.ibm.com/support/pages/node/7057023).


### updateAuthAlias.py
[updateAuthAlias.py](https://github.com/WASdev/sample.wsadmin.websphere-traditional/blob/master/updateAuthAlias.py) dynamically updates the password of the specified JAAS authentication alias in a server process without requiring a server restart.  This script will not work as written on a node agent or deployment manager.

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

## License
Unless otherwise noted in a script:<br/>
[![License](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](https://www.apache.org/licenses/LICENSE-2.0)
