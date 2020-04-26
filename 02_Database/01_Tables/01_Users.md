# Users

<style>
tr > td:first-of-type {
  text-align: center;
}
</style>

Statuses:

- active - User is active
- inactive - User is inactive

<table>
  <tr>
    <th>Columns</th>
    <th>Properties</th>
    <th>Description</th>
  </tr>
  <tr>
    <td>id</td>
    <td>
      <ul>
        <li>Integer</li>
        <li>Primary Key</li>
        <li>Auto-increment</li>
      </ul>
    </td>
    <td>Unique id</td>
  </tr>
  <tr>
    <td>name</td>
    <td>
      <ul>
        <li>Varchar2 (20)</li>
        <li>Not Null</li>
        <li>Check for name</li>
      </ul>
    </td>
    <td>User's name, must be a proper string</td>
  </tr>
  <tr>
    <td>surname</td>
    <td>
      <ul>
        <li>Varchar2 (20)</li>
        <li>Not Null</li>
        <li>Check for surname</li>
      </ul>
    </td>
    <td>User's surname, must be a proper string</td>
  </tr>
  <tr>
    <td>role</td>
    <td>
      <ul>
        <li>Varchar2 (20)</li>
        <li>Not Null</li>
      </ul>
    </td>
    <td>Role, defines functionality</td>
  </tr>
  <tr>
    <td>password</td>
    <td>
      <ul>
        <li>Varchar2 (400)</li>
        <li>Not Null</li>
      </ul>
    </td>
    <td>Encrypted password</td>
  </tr>
  <tr>
    <td>stats_id</td>
    <td>
      <ul>
        <li>Integer</li>
        <li>Not Null</li>
        <li>Unique</li>
        <li>Foreign Key</li>
      </ul>
    </td>
    <td>1 to 1 reference, Each user has one and only one row of his statistics. See <a href="./02_UserStats.md">User Stats</a></td>
  </tr>
  <tr>
    <td>gender</td>
    <td>
      <ul>
        <li>Integer</li>
        <li>Not Null</li>
        <li>Check</li>
      </ul>
    </td>
    <td>1 for male, 0 for female</td>
  </tr>
  <tr>
    <td>phone</td>
    <td>
      <ul>
        <li>Varchar2 (10)</li>
        <li>Not Null</li>
        <li>Unique</li>
        <li>Check for phone number</li>
      </ul>
    </td>
    <td>Kazakhstan's phone number</td>
  </tr>
  <tr>
    <td>avatar</td>
    <td>
      <ul>
        <li>Varchar2 (200)</li>
        <li>Not Null</li>
      </ul>
    </td>
    <td>Image's hash sum</td>
  </tr>
  <tr>
    <td>birthday</td>
    <td>
      <ul>
        <li>Date</li>
        <li>Not Null</li>
      </ul>
    </td>
    <td>User's birthday</td>
  </tr>
  <tr>
    <td>status</td>
    <td>
      <ul>
        <li>Varchar2 (20)</li>
        <li>Not Null</li>
      </ul>
    </td>
    <td>Row status</td>
  </tr>
</table>
