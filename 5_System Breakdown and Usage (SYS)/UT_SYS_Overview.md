# Overview of Unit Test Cases | System Breakdown and Usage

*Legend:* #: number of elements | Y: Yes, number pending UT finalization | TBD: To Be Defined during the UT finalization

<table class="tg">
<thead>
  <tr>
    <th class="tg-wa1i"> </th>
    <th class="tg-wa1i"> </th>
    <th class="tg-wu5t">UT_SYS_1</th>
    <th class="tg-wu5t">UT_SYS_2</th>
    <th class="tg-wu5t">UT_SYS_3</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-wa1i"> </td>
    <td class="tg-wu5t">Dataset provider</td>
    <td class="tg-nrix">RFI</td>
    <td class="tg-nrix">RFI</td>
    <td class="tg-nrix">RFI</td>
  </tr>
  <tr>
    <td class="tg-wa1i"> </td>
    <td class="tg-wu5t">IFC reference file availabe</td>
    <td class="tg-nrix">Y</td>
    <td class="tg-nrix">Y</td>
    <td class="tg-nrix">Y</td>
  </tr>
  <tr>
    <td class="tg-6o9b" rowspan="2">Domains coverage</td>
    <td class="tg-wu5t">Railway only / Cross-domain</td>
    <td class="tg-nrix">Railway only</td>
    <td class="tg-nrix">Railway only</td>
    <td class="tg-nrix">Railway only</td>
  </tr>
  <tr>
    <td class="tg-wu5t">Covered railway-domain</td>
    <td class="tg-nrix">Track</td>
    <td class="tg-nrix">Track</td>
    <td class="tg-nrix">Track</td>
  </tr>
  <tr>
    <td class="tg-6o9b" rowspan="4">Usage</td>
    <td class="tg-wu5t">Groups of elements</td>
    <td class="tg-nrix">3</td>
    <td class="tg-nrix">3</td>
    <td class="tg-nrix">3</td>
  </tr>
  <tr>
    <td class="tg-wu5t">Groups of groups</td>
    <td class="tg-nrix">3</td>
    <td class="tg-nrix">3</td>
    <td class="tg-nrix">3</td>
  </tr>
    <td class="tg-wu5t">Group referenced in spatial element</td>
    <td class="tg-nrix">0</td>
    <td class="tg-nrix">1</td>
    <td class="tg-nrix">0</td>
  </tr>
   </tr>
    <td class="tg-wu5t">Pset associated to groups</td>
    <td class="tg-nrix">0</td>
    <td class="tg-nrix">0</td>
    <td class="tg-nrix">Y</td>
  </tr>
  <tr>
    <td class="tg-v1ns" rowspan="5">Relationships </td>
    <td class="tg-wu5t">RelAssignsToGroup</td>
    <td class="tg-nrix">5</td>
    <td class="tg-nrix">5</td>
    <td class="tg-nrix">5</td>
  </tr>
  <tr>
    <td class="tg-wu5t">RelContainedInSpatialStructure</td>
    <td class="tg-nrix">1</td>
    <td class="tg-nrix">1</td>
    <td class="tg-nrix">1</td>
  </tr>
  <tr>
    <td class="tg-wu5t">RelReferencedInSpatialStructure</td>
    <td class="tg-nrix">0</td>
    <td class="tg-nrix">1</td>
    <td class="tg-nrix">1</td>
  </tr>
  <tr>
    <td class="tg-wu5t">RelDefinesByProperty</td>
    <td class="tg-nrix">0</td>
    <td class="tg-nrix">0</td>
    <td class="tg-nrix">Y</td>
  </tr>
    <tr>
    <td class="tg-wu5t">RelDefinesByType</td>
    <td class="tg-nrix">0</td>
    <td class="tg-nrix">0</td>
    <td class="tg-nrix">0</td>
  </tr>
  <tr>
    <td class="tg-iu1v" rowspan="4">Included products</td>
    <td class="tg-wu5t">Systems</td>
    <td class="tg-nrix">2</td>
    <td class="tg-nrix">2</td>
    <td class="tg-nrix">2</td>
  </tr>
   <tr>
    <td class="tg-wu5t">Asset</td>
    <td class="tg-nrix">2</td>
    <td class="tg-nrix">2</td>
    <td class="tg-nrix">2</td>
  </tr>
  <tr>
    <td class="tg-wu5t">Assemblies</td>
    <td class="tg-nrix">0</td>
    <td class="tg-nrix">0</td>
    <td class="tg-nrix">0</td>
  </tr>
  <tr>
    <td class="tg-wu5t">Elements</td>
    <td class="tg-nrix">6</td>
    <td class="tg-nrix">6</td>
    <td class="tg-nrix">6</td>
  </tr>
</tbody>
</table>
