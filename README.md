# MAGNOLIA-8348: FreeMarker Restriction Bypass 3 in Magnolia CMS

An issue in the FreeMarker Filter of Magnolia CMS v6.2.17 and below allows attackers to bypass security restrictions and execute arbitrary code, read/write/move/copy/delete arbitrary files or launch DoS attacks via a crafted FreeMarker payload. Arbitrary code execution was successfully achieved via writing arbitrary JSP files.

### Collaboration:

This vulnerability was found in collaboration with Marian-Razvan Ilisanu.

### Vendor Disclosure:

The vendor's disclosure and fix for this vulnerability can be found [here](https://docs.magnolia-cms.com/product-docs/6.2/releases/release-notes-for-magnolia-cms-6.2.18/).

### Why no CVE?

Neither me nor the vendor requested a CVE for these vulnerabilities.

### Proof Of Concept:

More details and the exploitation process can be found in this [PDF](https://github.com/mbadanoiu/MAGNOLIA-8348/blob/main/Magnolia%20CMS%20-%20MAGNOLIA-8348.pdf).

### Additional Resources:

The "servletContenxt" SSTI gadget that results in the execution of arbitrary system commands was insired by this [advisory](https://securitylab.github.com/advisories/GHSL-2020-050-pebble/)

The H2 "INIT=RUNSCRIPT" payload was taken from this [blog post](https://blog.doyensec.com/2019/07/22/jackson-gadgets.html)

The JSP code used to execute arbitrary system commands can be found [here](https://gist.github.com/nikallass/5ceef8c8c02d58ca2c69a29a92d2f461)
