# Deploying-Active-Directory
<h2>Part 1: Active Directory Setup and Client Domain Join</h2>

<h3>1. Install Active Directory Domain Services</h3>

<ol>
  <li>
    <p>Login to the DC-1 virtual machine.</p>
  </li>
  <li>
    <p>Install the Active Directory Domain Services role.</p>
  </li>
  <li>
    <p>Promote the server to a Domain Controller, creating a new forest named <code>mydomain.com</code> (or your chosen domain name). Remember this domain name for subsequent steps.</p>
  </li>
  <li>
    <p>Restart the DC-1 virtual machine.</p>
  </li>
  <li>
    <p>Log back into DC-1 using the domain administrator account: <code>mydomain.com\labuser</code>.</p>
  </li>
</ol>

<h3>2. Create a Domain Administrator User</h3>

<ol>
  <li>
    <p>Open Active Directory Users and Computers (ADUC).</p>
  </li>
  <li>
    <p>Create a new Organizational Unit (OU) named <code>_EMPLOYEES</code>.</p>
  </li>
  <li>
    <p>Create a new OU named <code>_ADMINS</code>.</p>
  </li>
  <li>
    <p>Create a new user named "Jane Doe" with the following details:</p>
    <ul>
      <li><strong>Username:</strong> <code>jane_admin</code></li>
      <li><strong>Password:</strong> <code>Cyberlab123!</code></li>
    </ul>
  </li>
  <li>
    <p>Add the <code>jane_admin</code> user to the "Domain Admins" security group.</p>
  </li>
  <li>
    <p>Log out or close the connection to DC-1.</p>
  </li>
  <li>
    <p>Log back into DC-1 using the <code>mydomain.com\jane_admin</code> account. Use this account for subsequent administrative tasks.</p>
  </li>
</ol>

<h3>3. Join Client-1 to the Domain</h3>

<ol>
  <li>
    <p><strong>Note:</strong> Client-1's DNS settings and restart have already been performed in previous steps.</p>
  </li>
  <li>
    <p>Login to Client-1 using the local administrator account: <code>labuser</code>.</p>
  </li>
  <li>
    <p>Join Client-1 to the <code>mydomain.com</code> domain. The computer will restart.</p>
  </li>
  <li>
    <p>Login to the Domain Controller (DC-1) using <code>mydomain.com\jane_admin</code>.</p>
  </li>
  <li>
    <p>Open Active Directory Users and Computers (ADUC) and verify that Client-1 is listed.</p>
  </li>
  <li>
    <p>Create a new OU named <code>_CLIENTS</code>.</p>
  </li>
  <li>
    <p>Drag the Client-1 computer object into the <code>_CLIENTS</code> OU.</p>
  </li>
</ol>
