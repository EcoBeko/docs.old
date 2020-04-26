# Waste Types

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
    <td>title</td>
    <td>
      <ul>
        <li>Varchar2 (50)</li>
        <li>Not Null</li>
        <li>Unique</li>
      </ul>
    </td>
    <td>Waste's title</td>
  </tr>
  <tr>
    <td>types</td>
    <td>
      <ul>
        <li>Varchar2 (30)</li>
        <li>Not Null</li>
      </ul>
    </td>
    <td>Types, separated by comma</td>
  </tr>
  <tr>
    <td>icon</td>
    <td>
      <ul>
        <li>Varchar2 (200)</li>
        <li>Not Null</li>
      </ul>
    </td>
    <td>Image hash sum</td>
  </tr>
  <tr>
    <td>mark</td>
    <td>
      <ul>
        <li>Varchar2 (20)</li>
        <li>Not Null</li>
      </ul>
    </td>
    <td>Waste's mark</td>
  </tr>
</table>
