# Header Schemas

XML schemas for representing headers for email, MIME, and others.

This project seeks to allow developers of [XML schemas](https://www.w3.org/XML/Schema) to reference
[headers](https://www.iana.org/assignments/message-headers/message-headers.xhtml) from various protocols in their work.
For example, the project that motivated this work is the [Email Forensics XML (EFXML)
project](https://bitbucket.org/jpaglier/efxml), which, in part, defines a schema to represent email headers in such a
way as to be useful in forensic examinations. The EFXML schema defines elements for provenance, type of mailbox, and so
forth, but all the header fields are defined here.


## Protocols

Currently, the following protocols have been documented in this project:

- `mail`
- `MIME`
- `none`

From the [list provided by IANA](https://www.iana.org/assignments/message-headers/message-headers.xhtml), there are two
protocols that have not yet been documented here:

- `http`
- `netnews`

I would appreciate any help given to document these! Please just make sure to include `annotation` tags for each header
element entry with the following information:

- `appinfo` that contains a `<header/>` tag (defined in the [header
  info](https://github.com/mmabey/header_schemas/blob/master/header_info.xsd) schema). Should contain accurate
  information about the RFCs that define the header.
- `documentation` that contains:
  - Documentation from the defining RFC/RFCs that describe the purpose of the header
  - Specification document(s): List of RFCs that define the header. This is a human-readable format of the data given in
    the `<header/>` tag
  - Type: Should be "Permanent" or "Provisional"
  - Status: Should be "unknown", "standard", "reserved", "deprecated", "obsolete", "informational", "standards-track",
    "work-in-progress", or "experimental". This is decided by the documentation of the header in the specifying RFC.

For examples of the above information, just check the `header_info.xsd`, `email_headers.xsd`, or `mime_headers.xsd`
schemas.


## License

All code in this project is released under the MIT License. See
[LICENSE](https://github.com/mmabey/header_schemas/blob/master/LICENSE) for more details.
