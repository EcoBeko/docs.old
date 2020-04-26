# User Statistics

<style>
tr > td:first-of-type {
  text-align: center;
}
</style>

Statuses:

- active - Statistics could be used
- inactive - No use

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
    <td>trees</td>
    <td>
      <ul>
        <li>Number</li>
        <li>Not Null</li>
      </ul>
    </td>
    <td>Amount of Trees saved</td>
  </tr>
  <tr>
    <td>Energy</td>
    <td>
      <ul>
        <li>Number</li>
        <li>Not Null</li>
      </ul>
    </td>
    <td>Amount of Energy saved</td>
  </tr>
  <tr>
    <td>waste</td>
    <td>
      <ul>
        <li>Number</li>
        <li>Not Null</li>
      </ul>
    </td>
    <td>Amount of waste collected</td>
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
