.. _iworkflow_managed_device:


iworkflow_managed_device - Manipulate cloud managed devices in iWorkflow
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. versionadded:: 2.4


.. contents::
   :local:
   :depth: 2


Synopsis
--------

* Manipulate cloud managed devices in iWorkflow.


Requirements (on host that executes module)
-------------------------------------------

  * f5-sdk >= 1.5.0
  * iWorkflow >= 2.1.0


Options
-------

.. raw:: html

    <table border=1 cellpadding=4>
    <tr>
    <th class="head">parameter</th>
    <th class="head">required</th>
    <th class="head">default</th>
    <th class="head">choices</th>
    <th class="head">comments</th>
    </tr>
                <tr><td>device<br/><div style="font-size: small;"></div></td>
    <td>yes</td>
    <td></td>
        <td></td>
        <td><div>Hostname or IP address of the device to manage in iWorkflow.</div>        </td></tr>
                <tr><td>password_credential<br/><div style="font-size: small;"></div></td>
    <td>yes</td>
    <td></td>
        <td></td>
        <td><div>Password of the user provided in <code>username_credential</code>.</div>        </td></tr>
                <tr><td>state<br/><div style="font-size: small;"></div></td>
    <td>no</td>
    <td>present</td>
        <td><ul><li>present</li><li>absent</li></ul></td>
        <td><div>Whether the managed device should exist, or not, in iWorkflow.</div>        </td></tr>
                <tr><td>username_credential<br/><div style="font-size: small;"></div></td>
    <td>yes</td>
    <td></td>
        <td></td>
        <td><div>Username credential used to log in to the remote device's REST interface. Note that this is usually different from the credential used to log into the CLI of the device.</div>        </td></tr>
        </table>
    </br>



Examples
--------

 ::

    
    - name: Discover a BIG-IP device with hostname lb.mydomain.com
      iworkflow_device:
          device: "lb.mydomain.com
          username_credential: "admin"
          password_credential: "admin"
          password: "secret"
          server: "mgmt.mydomain.com"
          user: "admin"
      delegate_to: localhost



Notes
-----

.. note::
    - Requires the f5-sdk Python package on the host. This is as easy as pip install f5-sdk.
    - For more information on using Ansible to manage F5 Networks devices see https://www.ansible.com/ansible-f5.



Status
~~~~~~

This module is flagged as **preview** which means that it is not guaranteed to have a backwards compatible interface.


Support
~~~~~~~

This module is community maintained without core committer oversight.

For more information on what this means please read :doc:`/usage/support`


For help developing modules, should you be so inclined, please read :doc:`Getting Involved </development/getting-involved>`, :doc:`Writing a Module </development/writing-a-module>` and :doc:`Guidelines </development/guidelines>`.