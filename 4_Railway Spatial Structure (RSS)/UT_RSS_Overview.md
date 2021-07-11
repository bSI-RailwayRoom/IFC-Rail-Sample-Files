# Overview of Unit Test Cases | Railway Spatial Structure

*Legend:* #: number of elements | Y: Yes, number pending UT finalization | TBD: To Be Defined during the UT finalization

<table class="tg">
<thead>
  <tr>
    <th class="tg-wa1i"> </th>
    <th class="tg-wa1i"> </th>
    <th class="tg-wu5t">UT_RSS_1</th>
    <th class="tg-wu5t">UT_RSS_2</th>
    <th class="tg-wu5t">UT_RSS_3</th>
    <th class="tg-wu5t">UT_RSS_4</th>
    <th class="tg-wu5t">UT_RSS_5</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-wa1i"> </td>
    <td class="tg-wu5t">Dataset provider</td>
    <td class="tg-nrix">RFI</td>
    <td class="tg-nrix">MINnD</td>
    <td class="tg-nrix">MINnD</td>
    <td class="tg-nrix">Nordic</td>
    <td class="tg-nrix">MINnD</td>
  </tr>
  <tr>
    <td class="tg-wa1i"> </td>
    <td class="tg-wu5t">IFC reference file availabe</td>
    <td class="tg-nrix">NO</td>
    <td class="tg-nrix">WIP</td>
    <td class="tg-nrix">WIP</td>
    <td class="tg-nrix">NO</td>
    <td class="tg-nrix">TBD</td>
  </tr>
  <tr>
    <td class="tg-6o9b" rowspan="2">Domains coverage</td>
    <td class="tg-wu5t">Railway only / Cross-domain</td>
    <td class="tg-nrix">Railway only</td>
    <td class="tg-nrix">Cross-domain</td>
    <td class="tg-nrix">Cross-domain</td>
    <td class="tg-nrix">Cross-domain</td>
    <td class="tg-nrix">TBD</td>
  </tr>
  <tr>
    <td class="tg-wu5t">Covered railway-domain</td>
    <td class="tg-nrix">Track</td>
    <td class="tg-nrix">Railway</td>
    <td class="tg-nrix">Track</td>
    <td class="tg-nrix">Track</td>
    <td class="tg-nrix">Track</td>
  </tr>
  <tr>
    <td class="tg-v1ns" rowspan="4">Relationships </td>
    <td class="tg-wu5t">RelAggregates</td>
    <td class="tg-nrix">3</td>
    <td class="tg-nrix">Y</td>
    <td class="tg-nrix">Y</td>
    <td class="tg-nrix">9</td>
    <td class="tg-nrix">Y</td>
  </tr>
  <tr>
    <td class="tg-wu5t">RelContainedInSpatialStructure</td>
    <td class="tg-nrix">0</td>
    <td class="tg-nrix">0</td>
    <td class="tg-nrix">0</td>
    <td class="tg-nrix">0</td>
    <td class="tg-nrix">Y</td>
  </tr>
  <tr>
    <td class="tg-wu5t">RelReferencedInSpatialStructure</td>
    <td class="tg-nrix">1</td>
    <td class="tg-nrix">Y</td>
    <td class="tg-nrix">Y</td>
    <td class="tg-nrix">0</td>
    <td class="tg-nrix">TBD</td>
  </tr>
  <tr>
    <td class="tg-wu5t">RelInterferesElements</td>
    <td class="tg-nrix">2</td>
    <td class="tg-nrix">0</td>
    <td class="tg-nrix">TBD</td>
    <td class="tg-nrix">2</td>
    <td class="tg-nrix">TBD</td>
  </tr>
  <tr>
    <td class="tg-f7c5" rowspan="5">IfcFacility</td>
    <td class="tg-wu5t">Railway</td>
    <td class="tg-nrix">3</td>
    <td class="tg-nrix">Y</td>
    <td class="tg-nrix">Y</td>
    <td class="tg-nrix">1</td>
    <td class="tg-nrix">Y</td>
  </tr>
  <tr>
    <td class="tg-wu5t">Bridge</td>
    <td class="tg-nrix">0</td>
    <td class="tg-nrix">0</td>
    <td class="tg-nrix">0</td>
    <td class="tg-nrix">0</td>
    <td class="tg-nrix">0</td>
  </tr>
  <tr>
    <td class="tg-wu5t">Road</td>
    <td class="tg-nrix">0</td>
    <td class="tg-nrix">7</td>
    <td class="tg-nrix">Y</td>
    <td class="tg-nrix">1</td>
    <td class="tg-nrix">Y</td>
  </tr>
  <tr>
    <td class="tg-wu5t">MarineFacility</td>
    <td class="tg-nrix">0</td>
    <td class="tg-nrix">0</td>
    <td class="tg-nrix">0</td>
    <td class="tg-nrix">0</td>
    <td class="tg-nrix">0</td>
  </tr>
  <tr>
    <td class="tg-wu5t">Building</td>
    <td class="tg-nrix">0</td>
    <td class="tg-nrix">0</td>
    <td class="tg-nrix">0</td>
    <td class="tg-nrix">0</td>
    <td class="tg-nrix">TBD</td>
  </tr>
  <tr>
    <td class="tg-h8xm" rowspan="6">IfcFacilityPart</td>
    <td class="tg-wu5t">RailwayPart</td>
    <td class="tg-nrix">7</td>
    <td class="tg-nrix">0</td>
    <td class="tg-nrix">TBD</td>
    <td class="tg-nrix">3</td>
    <td class="tg-nrix">Y</td>
  </tr>
  <tr>
    <td class="tg-wu5t">BridgePart</td>
    <td class="tg-nrix">0</td>
    <td class="tg-nrix">0</td>
    <td class="tg-nrix">0</td>
    <td class="tg-nrix">0</td>
    <td class="tg-nrix">0</td>
  </tr>
  <tr>
    <td class="tg-wu5t">RoadPart</td>
    <td class="tg-nrix">0</td>
    <td class="tg-nrix">0</td>
    <td class="tg-nrix">0</td>
    <td class="tg-nrix">3</td>
    <td class="tg-nrix">TBD</td>
  </tr>
  <tr>
    <td class="tg-wu5t">MarineFacilityPart</td>
    <td class="tg-nrix">0</td>
    <td class="tg-nrix">0</td>
    <td class="tg-nrix">0</td>
    <td class="tg-nrix">0</td>
    <td class="tg-nrix">0</td>
  </tr>
  <tr>
    <td class="tg-wu5t">CommonPart</td>
    <td class="tg-nrix">0</td>
    <td class="tg-nrix">0</td>
    <td class="tg-nrix">0</td>
    <td class="tg-nrix">0</td>
    <td class="tg-nrix">0</td>
  </tr>
  <tr>
    <td class="tg-wu5t">BuildingStorey</td>
    <td class="tg-nrix">0</td>
    <td class="tg-nrix">0</td>
    <td class="tg-nrix">0</td>
    <td class="tg-nrix">0</td>
    <td class="tg-nrix">0</td>
  </tr>
  <tr>
    <td class="tg-uimp"> </td>
    <td class="tg-wu5t">SpatialZone</td>
    <td class="tg-nrix">1</td>
    <td class="tg-nrix">0</td>
    <td class="tg-nrix">Y</td>
    <td class="tg-nrix">0</td>
    <td class="tg-nrix">TBD</td>
  </tr>
  <tr>
    <td class="tg-3wnp"> </td>
    <td class="tg-wu5t">IfcSpace</td>
    <td class="tg-nrix">0</td>
    <td class="tg-nrix">0</td>
    <td class="tg-nrix">0</td>
    <td class="tg-nrix">0</td>
    <td class="tg-nrix">0</td>
  </tr>
  <tr>
    <td class="tg-iu1v" rowspan="3">Included products</td>
    <td class="tg-wu5t">Systems</td>
    <td class="tg-nrix">0</td>
    <td class="tg-nrix">0</td>
    <td class="tg-nrix">TBD</td>
    <td class="tg-nrix">0</td>
    <td class="tg-nrix">0</td>
  </tr>
  <tr>
    <td class="tg-wu5t">Assemblies</td>
    <td class="tg-nrix">0</td>
    <td class="tg-nrix">0</td>
    <td class="tg-nrix">0</td>
    <td class="tg-nrix">0</td>
    <td class="tg-nrix">TBD</td>
  </tr>
  <tr>
    <td class="tg-wu5t">Elements</td>
    <td class="tg-nrix">0</td>
    <td class="tg-nrix">0</td>
    <td class="tg-nrix">0</td>
    <td class="tg-nrix">0</td>
    <td class="tg-nrix">TBD</td>
  </tr>
</tbody>
</table>
