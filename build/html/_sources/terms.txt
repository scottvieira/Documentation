Terms Tool User Guide
---------------------

 ### About the CORAL Terms Tool

 An add-on to CORAL Licensing, the Terms Tool enables key stakeholders
 such as interlibrary loan staff to view the license terms without
 needing direct access to CORAL Licensing. The tool allows authorized
 users to retrieve license terms for a specific resource based on an
 ISSN or ISBN query. In addition to CORAL Licensing, the Terms Tool
 requires the installing site to have either the SFX or
 SerialsSolutions openURL resolver (or alternatively any openURL
 resolver with an API). The Terms Tool queries the openURL resolver for
 a specific ISSN or ISBN, retrieves the list of available providers for
 that ISSN/ISBN, and then queries CORAL Licensing for the license terms
 for each provider. It is a multi-step process but it all takes place
 behind the scenes and results in a seamless easy to use process for
 the user.

### Enabling the Terms Tool

 The process of using the Terms Tool begins with the license record
 within CORAL Licensing. The first step is for the licensing personnel
 to create a license record with completed expressions as in the
 following screenshot.

 Please note that these are not the actual license terms for Allen
 Press journals. This is only a fabricated example. This license record
 shows both the Coursepacks and Interlibrary Loan expressions for the
 license agreement titled *Allen Press Online Journals Terms and
 Conditions of Use*. There are two important items to note about these
 expressions that directly impact the terms tool. The first is that the
 expressions are using Display Notes rather than Internal Notes. Each
 expression type can be configured within the CORAL Licensing Admin tab
 to use either Display or Internal Notes. Only those expressions which
 use Display Notes are made available through the Terms Tool. The
 second item of note is the presence of the checkbox next to the
 expression type. This is the Terms Tool Checkbox. It is used by the
 licensing personnel to indicate that the expression is completed and
 is ready to be included in the Terms Tool. The action of checking this
 box will send out an email to the personnel managing the Terms Tool

 alerting them that new license terms are available. The recipients of
 this email are configured on the Admin tab of CORAL Licensing. The
 following screenshot shows the details of a user entry in CORAL
 Licensing. Any user with an email address in the ‘Terms Tool Email’
 field will receive the system generated email when the terms tool
 checkbox is selected.

### Mapping License Terms to Resources

 At this point there is a completed license record showing the terms
 for the license agreement *Allen Press Online Journals Terms and
 Conditions of Use*. The next step which needs to be completed is to
 identify which journals are covered by this specific license
 agreement. This is accomplished using the ‘Terms Tool’ tab on the
 license record as in the following screenshot.

 The task is to identify which journals are covered by the *Allen Press
 Online Journals and Conditions of Use* license agreement. This is
 accomplished by making a connection between the license agreement and
 the list of journals as entered in the library’s openURL resolver. In
 this example all of the journals that are covered by the terms of the
 agreement were activated and entered as a distinct group within the
 library’s openURL resolver. In SFX for example this is accomplished by
 activating all the journals covered by the agreement within the same
 target. The target is then given a target public name of ‘Allen Press’
 (serialsolutions calls this field databaseName). Then within the
 ‘Terms Tool’ tab of CORAL Licensing the link can be entered between
 the document *Allen Press Online Journals and Conditions of Use* and
 the SFX target named ‘Allen Press’. The Terms Tool will now know that
 all journals available within the Allen Press target are covered by
 the terms of this specific license agreement.

 The Terms Tool now has the information it needs to operate. The
 scenario is as follows. The Terms Tool receives an ISSN via the url
 *http://.../coral/terms/?issn=XXXX-XXXX*. The Terms Tool sends a query
 with the provided issn to the library’s openURL resolver. The openURL
 resolver returns an xml reply listing all of the provider names (SFX’s
 target public name or SerialsSolutions’ databaseName) for the provided
 ISSN. The Terms Tool queries CORAL Licensing for all license
 agreements which have been mapped to each provider name and retrieves
 all of the associated license terms from the identified license
 agreements. The terms are then displayed on screen to the user.

### Terms Tool in Action

 The following screenshot shows the Terms Tool display for the journal
 *Intellectual and Developmental Disabilities* (issn 1934-9491).

 At this point the Terms Tool has already queried both the openURL
 resolver and then CORAL Licensing and identified that Coursepack and
 Interlibrary Loan terms are available for this journal. The link for
 Interlibrary Loan leads to the following screenshot.

 And in the above screenshot the user now sees the specific
 interlibrary loan license terms for this journal. Access to this
 journal is available via Allen Press and interlibrary loan use is
 permitted. The Display Notes from the license record detail how the
 interlibrary loan is to be handled. The actual document text from the
 license agreement is hidden beneath a ‘view license snippet’ link for
 those wishing to see the original language. The provider name at the
 end of the opening line is hyperlinked and will take the user directly
 to the provider’s webpage for the journal. This example lists only one
 provider, Allen Press, but the Terms Tool will display terms for all
 providers when the library does have

 access through multiple providers. If no license terms are available
 for a provider the Terms Tool will show that as well as in the
 following example.

Again, please note that the license terms in these screenshots are all
fabricated examples and do not reflect the actual terms of the
provider’s real license agreements. In the preceding screenshot access
is available to the library through multiple providers but license terms
are only available for the BioMed Central access.

### Finding the Terms Tool

 The Terms Tool is used by querying it with a url containing either an
 ISSN or ISBN such as
 [*http://coral.mylibrary.edu/coral/terms/?issn=XXXX-XXXX*.](http://coral.mylibrary.edu/coral/terms?issn=XXXX-XXXX)
 Using the Terms Tool requires some way for users to easily send this
 type of ISSN/ISBN query. One option is to place a link to the Terms
 Tool on the library’s openURL resolver menu. The template for the SFX
 menu, for instance, can be edited in such a way as to create a link to
 the Terms Tool which will dynamically use the ISSN and/or ISBN for the
 specific resource being requested. The University of Notre Dame chose
 this option and implemented the Terms Tool by placing the necessary
 code in the footer of the SFX menu template. Similar options should
 exist for the SerialsSolutions openURL resolver. A number of options
 exist for how the Terms Tool could be implemented. It will be up to
 each library to determine how they wish to create the necessary
 ISSN/ISBN links.

### Technical Documentation

 Additional technical documentation for installing and implementing the
 Terms Tool is available on the CORAL Documentation page. Please read
 the technical documentation thoroughly as it explains additional
 details and configuration options necessary for proper use of the
 Terms Tool.
