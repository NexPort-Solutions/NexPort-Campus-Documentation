# NexPort Campus v6.6.5 Release Notes

### New Features <a href="#_6zg6y82t1f6i" id="_6zg6y82t1f6i"></a>

#### Certificate Templates have a WYSIWYG editor option (55851) <a href="#_3hnom0nshyvg" id="_3hnom0nshyvg"></a>

Admins can create Html Certificate Templates in Manage Campus Certificates Organization Tool. This new feature will make it easier for certificate editors to edit and maintain certificates directly in NexPort.

Certificate editors will no longer need to use a PDF editor to make changes to their certificate templates. Certificate Templates can have multiple pages and they can be laid out in either a portrait or landscape style. Here are a few features of the new certificate editor:

* Support for multiple pages.
* Use tables to control precisely the look and feel of certificates.
* Assign background images to certificates.
* Use and number of images in the layout
* Edit raw HTML and CSS
* Preview the final PDF Version.

{% content-ref url="../../administrator-documentation/administrator-reference/campus-management/organization-tools/certificates/" %}
[certificates](../../administrator-documentation/administrator-reference/campus-management/organization-tools/certificates/)
{% endcontent-ref %}

#### Ability to export test questions in same format as "Question Upload Template" (152421) <a href="#_ktqvg95ppz0f" id="_ktqvg95ppz0f"></a>

Question bank administrators can now export a question bank to an excel spreadsheet. The sheet is in the same format as the upload spreadsheet. This would allow exporting a question bank elsewhere or editing outside of NexPort then uploading again.

#### Training Plans and Sections should list the catalogs they are in (151745) <a href="#_gorrzaz1a98s" id="_gorrzaz1a98s"></a>

Administrators can now see a listing of all catalogs a training plan or section is assigned to.

#### Media Library Management should be its own tool in Manage Campus (150133) <a href="#_s357wlhszrnj" id="_s357wlhszrnj"></a>

Added Media Library as a Group Tool in Manage Campus. The Media Library is moved out of the Documents tool and is now its own tool.

### Enhancements <a href="#_ro0uwulvjzcp" id="_ro0uwulvjzcp"></a>

#### NexPort Documentation and Help area is being moved to the new NexPort Knowledgebase (153733) <a href="#_9g3tp1axq42n" id="_9g3tp1axq42n"></a>

All end user documentation for NexPort Campus has moved to our new site at [https://docs.nexportsolutions.com](https://docs.nexportsolutions.com/)

The new documentation site will allow us to more quickly update documentation, provide better search and improve navigation.

#### Add direct links to the catalogs in the catalog link listing for Training Plans and Sections (151926) <a href="#_8c2cekuf4ba3" id="_8c2cekuf4ba3"></a>

The catalog listing for each section and training plan now allows administrators to click on a catalog title and go directly to that catalog.

![](../../.gitbook/assets/0)

#### Section and Training Plan editors need to show the Date Modified and Date Created (151562) <a href="#_xdy1b0au1pby" id="_xdy1b0au1pby"></a>

Date created and date modified are displayed on the Training plan and Section details pages.

#### Training Plan AND Section Academic Override view in User Profile needs additional information (151561) <a href="#_6b0bywsy33gk" id="_6b0bywsy33gk"></a>

The individual enrollment views for both Training Plans and Sections now display additional information including Unique Name, Enrollment Organization, Syllabus Organization and Section Title.

![](../../.gitbook/assets/1)

![](../../.gitbook/assets/2)

All new display items are hyperlinked to the resource they represent. This will allow administrators to quickly move between an enrollment view and the various other resources it links to including the organization, section or training plan editors.

#### Implement Mobile UI Enhancements for the Courseware player (150047) <a href="#_350ixswo8ova" id="_350ixswo8ova"></a>

The courseware player will now give SCORM courses more real-estate to use. The overall UI is more responsive and will display better on a mobile device.

#### Disable Session State for Controllers that do not require it (150045) <a href="#_n29h3csxpp7l" id="_n29h3csxpp7l"></a>

This increases the performance of many parts of NexPort Campus by removing unnecessary work to generate most student views.

#### Convert Controller to MVC :ScormController (56097) <a href="#_f72t57yypm1v" id="_f72t57yypm1v"></a>

Upgrading the SCORM player components and addressing performance issues.

#### Assignments for Instructor should use the media library for images (149227) <a href="#_epaxko0yv0r" id="_epaxko0yv0r"></a>

Editing or creating an assignment uses the media library for images instead of source urls.

#### Administrators Should be able to Set Background Image for HTML Certificate Templates (151409) <a href="#_x582mkbk689d" id="_x582mkbk689d"></a>

Added the option for Html Certificate Templates to have a background image.

#### Admins need to know more about Test assignment tests (152694) <a href="#_i5jdpw98uubf" id="_i5jdpw98uubf"></a>

Admins who edit or create a Test Assignment will now see an org link and test details link for the selected test.

#### Instructors should be able to view their inbox from the new instructor view (88453) <a href="#_fe6qp1fnjlx2" id="_fe6qp1fnjlx2"></a>

#### Student Profile Enrollment listing needs more information (151560) <a href="#_6yr29nqijwbd" id="_6yr29nqijwbd"></a>

The enrollment listing in the student profile now shows last activity date, the organization column includes links to the organizations the enrollment belongs to and admins can link directly to the editor for the section or training plan the enrollment belongs to.

#### Welcome Letters should be processed by the notifications job using a queue item (150698) <a href="#_jtyi1o43i3ef" id="_jtyi1o43i3ef"></a>

Welcome letter processing will happen more reliably as a background worker.

#### HTML Certificate Templates Should Embed Images and Background Images (149982) <a href="#_9cgvqrjej2ai" id="_9cgvqrjej2ai"></a>

The new HTML based certificate template editor will allow editors to embed inline and background images.

#### Document the MathJax syntax (116462) <a href="#_9jeg7b4illll" id="_9jeg7b4illll"></a>

MathJax is a display engine for mathematics. It allows editors to write mathematical notations with built-in support for screen readers. The notation can be written in LaTex, Tex, MathML, and AsciiMath and it allows curriculum designers to create user-friendly symbols, equations, and any mathematical figure. For more information on MathJax, see mathjax.org.. Extended MathJax documentation can be found in the [Administrator Documentation](https://docs.nexportsolutions.com/nexport-user-documentation/administrator-documentation/administrator-reference/mathjax-reference).

### Defects (Bugs) <a href="#_7lwiih2j212y" id="_7lwiih2j212y"></a>

#### When updating an HTML certificate, Ajax error is thrown after selecting edit page (152279) <a href="#_6koo9364jdh1" id="_6koo9364jdh1"></a>

#### Random broken image icons (151378) <a href="#_xmdo0t7syv8w" id="_xmdo0t7syv8w"></a>

#### Purchases Tab in User Profile Throws Error When Loading More (153614) <a href="#_b7lcpdbz6ssp" id="_b7lcpdbz6ssp"></a>

#### Cleanup SOLR settings that are not used AND add indexes disk to solr index server (151611) <a href="#_dise3wpmc3y2" id="_dise3wpmc3y2"></a>

#### Section titles replaced with System IDs in Catalog Views (154164) <a href="#_ml2ulsyz8y35" id="_ml2ulsyz8y35"></a>

#### Discussion Assignment Add Topic Fails to Load TinyMCE Text Area for Title and Content (154130) <a href="#_m3k7gq3iplal" id="_m3k7gq3iplal"></a>

#### Save Assignment in Instructor Classroom throws TinyMCE is Not a Function (154128) <a href="#_ile22zj9u4is" id="_ile22zj9u4is"></a>

#### Select Test with Org that has Special Characters Throws Error when Creating/Editing a Test Assignment in Beta (154123) <a href="#_79jrxvqc7sza" id="_79jrxvqc7sza"></a>

#### Edit/Create Assignments Loading Dialog Should Not Have Scroll Bar Show Up (150116) <a href="#_p7vc53yw3ouf" id="_p7vc53yw3ouf"></a>

Removed a user interface issue for creating or editing assignments where the loading dialog had a scroll bar.

#### Failing to Generate Certificate Thumbnail Should Gracefully Set Default (150119) <a href="#_hyptyaiukt7" id="_hyptyaiukt7"></a>

Certificate Template thumbnails will have a default image as their thumbnail if the thumbnail fails to get generated or if there are no Pages in a Html Certificate Template.

#### HTML Certificate Templates Custom Fields Should Not Allow Dot '.' Character (151037) <a href="#_hjym90qnxc21" id="_hjym90qnxc21"></a>

Admins who are creating or altering Html Certificate Template Custom Fields are warned when using the dot '.' character.

#### Exception Thrown When Updating Certificate Template with No Custom Fields (151105) <a href="#_bqcjeng1yrtn" id="_bqcjeng1yrtn"></a>

Admins who are creating or altering Certificate Template Custom Fields are warned when a Value is added without a Key.

#### Adding identical Key name should provide Prompt when Save (151421) <a href="#_avnlnm4a2l7v" id="_avnlnm4a2l7v"></a>

Admins creating or altering a Certificate Template with Custom Fields are warned when a duplicate Key is added.

#### Html Certificate Template Help Icon Should be On Page Dialog (151812) <a href="#_i3yxndz3vodl" id="_i3yxndz3vodl"></a>

Html Certificate Templates have a help icon to allow Admins to search for template properties.

#### View Transcript As Admin or Student Show Failed to Generate Certificate if Cert Queue Item Exists With Missing CustomFields (152958) <a href="#_58dlchpunp7n" id="_58dlchpunp7n"></a>

Transcript certificates that fail to be generated, with an Organization with 'Exception' option selected for Certificate Behavior in the Customize tool in Manage Campus, will show a list of missing custom fields when an admin tries to view the generated certificate.

#### If you go to the url for a NexPort org, that is not the root org, it redirects to the root org (150797) <a href="#_h03fn2iyn7n6" id="_h03fn2iyn7n6"></a>

Fixed issue with an orgs login url redirecting to root org.

#### nexport does not load when using a previously used ticket redemption link (153412) <a href="#_7kw1xrhl40yh" id="_7kw1xrhl40yh"></a>

Users who previously used a ticket redemption link will now be redirected to log in.

#### Select Item in Create New Invoice Throws Error (152965) <a href="#_wwkhimnkby5g" id="_wwkhimnkby5g"></a>

Fixed Create New Invoice error when selecting a user and clicking next.

#### Question banks should handle missing path more gracefully (148936) <a href="#_rcsakqz2ckq2" id="_rcsakqz2ckq2"></a>

#### Section Fulfillments have unexplained transcript record attached that does not belong to student (153710) <a href="#_8pqxk9p3todl" id="_8pqxk9p3todl"></a>

#### Rich text editors in Nexport Do Not Appear and can not find themes (150569) <a href="#_r0cm6byw1d8d" id="_r0cm6byw1d8d"></a>

#### Clicking the Contact Customer Service link does not load but instead returns you to the NexPort login page. (150656) <a href="#_rz08hnb3nsd0" id="_rz08hnb3nsd0"></a>

#### Store Media Location Race Condition in MediaAssignment Controller (150095) <a href="#_yu3h49465pu6" id="_yu3h49465pu6"></a>

#### Error occurs when editing some profiles that have no owner organization (150417) <a href="#_b3g8c57lldu" id="_b3g8c57lldu"></a>

#### Unable to Sort in the Documents area and receiving AJAX error when clicking on Sort by "Name" (151215) <a href="#_l097ejvzj0k" id="_l097ejvzj0k"></a>

#### Instructor Inbox intermittently slow (150162) <a href="#_bl0xa8sd5ih2" id="_bl0xa8sd5ih2"></a>

#### Organization links in the AO area for enrollments do not work (151925) <a href="#_e82faqlcl7yv" id="_e82faqlcl7yv"></a>

#### Duplicate validation for product mapping gives a bad error (150724) <a href="#_1u4um145avcd" id="_1u4um145avcd"></a>

#### Batch User Upload should not fail when the welcome letter fails to send (150697) <a href="#_7vkpwjiytlvt" id="_7vkpwjiytlvt"></a>

#### Complete Assignment often throws an error (148661) <a href="#_z9dyrp7jkdt2" id="_z9dyrp7jkdt2"></a>

#### Instructors receiving timeout errors (153326) <a href="#_gs57ln9e92ne" id="_gs57ln9e92ne"></a>

#### Nexport should reset the session for a user when they sign out or get signed out (152933) <a href="#_ydl8zr1cj9ju" id="_ydl8zr1cj9ju"></a>

#### Get Invoice Redemption API frequently times out (timeout) (153328) <a href="#_j9q3y7l6swxs" id="_j9q3y7l6swxs"></a>

#### Copy catalog displays a failure message if the send message system fails (153794) <a href="#_9ulv1a6u1npn" id="_9ulv1a6u1npn"></a>

#### Media Library Breaks and fails to load tabs after the second org selected with the tool (153626) <a href="#_gple6d1za86c" id="_gple6d1za86c"></a>

#### Object reference not set to an instance of an object when selecting Add User button on NexPort Beta (153169) <a href="#_li5hbamfmro1" id="_li5hbamfmro1"></a>

#### Script visible at the top of the screen after Toggle Profiler is clicked (153302) <a href="#_1kirsqwh1nfo" id="_1kirsqwh1nfo"></a>

#### HTML Certificate Templates Generated With "Exception" Org Option Should Behave the Same as PDF Certificate Templates (152899) <a href="#_x8oa2tmggtu0" id="_x8oa2tmggtu0"></a>

#### Warning message doesn't go away when navigating (151199) <a href="#_nn59m7st0pk8" id="_nn59m7st0pk8"></a>

#### Quickly navigating through assignments in the student classroom will cause a previously displayed assignment to show up (150208) <a href="#_n7sxks442cw5" id="_n7sxks442cw5"></a>

#### Rich text editor fails to load for question text on subsequent edits (152675) <a href="#_8dhuodyl6jy4" id="_8dhuodyl6jy4"></a>

#### Rich Text Editor Fails to Load on Support Request Email on Subsequent Loads (152964) <a href="#_fk7d8e9e8x9l" id="_fk7d8e9e8x9l"></a>

#### Rich Text Editor Fails to Load on Reply on Subsequent Loads (153050) <a href="#_ohqrgogahr1h" id="_ohqrgogahr1h"></a>

#### Rich Text Editor Fails to Load New Internal Mail Message On Second Attempt W/O Refresh (152962) <a href="#_r9d156sw9l1g" id="_r9d156sw9l1g"></a>

#### Table Properties fields and text bounce when clicking thru fields while clicking titles activates fields and drop downs (152084) <a href="#_733rxo6ms2gf" id="_733rxo6ms2gf"></a>

#### View Transcript as Admin or Student Should Show Still Generating if Cert Queue Item Exists (152040) <a href="#_se1xp7tenxjm" id="_se1xp7tenxjm"></a>

#### WebApi GetEnrollments should just return the error and not log an error log (150166) <a href="#_rbxqkxi0ljqv" id="_rbxqkxi0ljqv"></a>

#### Manage Campus Text Areas in Dialogs Do Not Focus Properly (Scrolls to Bottom on Right-Click, Dialog Popups are Uneditable, etc) (150284) <a href="#_96nhn11dp4do" id="_96nhn11dp4do"></a>

#### HTML Certificates Preview and Generation Should Follow Empty, Default, Throw Error Settings (151098) <a href="#_tzicgodde4nl" id="_tzicgodde4nl"></a>

#### Saving PDF template upload non PDF causes: Cannot apply indexing with \[] to an expression of type 'System.Dynamic.DynamicObject' (151062) <a href="#_bcdl9epcgron" id="_bcdl9epcgron"></a>

#### HTML Certificate Template Pages Should Constrain to Number of Pages and Not be Pushed Out of Bounds in Preview/Generate (151961) <a href="#_ahsrs7yqu7c8" id="_ahsrs7yqu7c8"></a>

#### HTML Certificate Templates Thumbnails not Generated (151036) <a href="#_3fxspubmq3gy" id="_3fxspubmq3gy"></a>

#### Training Plans showing Certificate None only (152621) <a href="#_f5f1gtj10avs" id="_f5f1gtj10avs"></a>

#### Error when select Edit Page btn in new HTML Template (151944) <a href="#_gky108jceui3" id="_gky108jceui3"></a>

#### Limit Certificate Thumbnail size in Section Cert Selection for No Image Available Case (150164) <a href="#_91ulkmr1dsbc" id="_91ulkmr1dsbc"></a>

#### Add New PAge to already existing certificate Keyboard actions cause white area to shrink/disappear (151759) <a href="#_og5u7sv72s23" id="_og5u7sv72s23"></a>

#### Edit Existing Certificates 1st Save causes Value field input to disappear while 2nd Save causes it to reappear (151296) <a href="#_w0ttq5ecthtj" id="_w0ttq5ecthtj"></a>

#### Edit/Create Certificate Template Pages Dialog Should be Full Screen (151808) <a href="#_2u8mn2532z41" id="_2u8mn2532z41"></a>

#### HTML Certificate Template Preview Throws Error for Template Membership Groups (151038) <a href="#_b7tjl7xt02oh" id="_b7tjl7xt02oh"></a>

#### certificate title links active without visible result (151752) <a href="#_mugg7g9luznq" id="_mugg7g9luznq"></a>

#### Edit/Create Certificate Template Page Source Code and Table Properties Should be Editable (151810) <a href="#_kzxu9pgxbb27" id="_kzxu9pgxbb27"></a>

#### When updating a completion certificate in the SHCOE Career Training org, we receive a ghost script Ghostscript conversion error (148722) <a href="#_m47ud57y12vf" id="_m47ud57y12vf"></a>

#### Manage Campus Customize Tool Text Area Throws Unexpected Sudo 'tinymce' In Manage Campus (151904) <a href="#_gifljuh9484l" id="_gifljuh9484l"></a>

#### Certificate Replacement tab is unavailable in some orgs (151146) <a href="#_vyh6ue5nmoe" id="_vyh6ue5nmoe"></a>

#### In Edit Page window, pressing ENTER key pushes cursor to bottom of page (151751) <a href="#_ajo2w0adyrkj" id="_ajo2w0adyrkj"></a>

#### Switching Layout Orientation on Html Certificate Template Should Warn the Changes Won't Take Effect Until You Save (151811) <a href="#_82gv1zmz4ou9" id="_82gv1zmz4ou9"></a>

#### When opening the Add user tab, an ajax error is immediately thrown. (151530) <a href="#_j7u5umysdv41" id="_j7u5umysdv41"></a>

#### A Sections Selected Certificate Highlights Incorrect Certificates Background (150335) <a href="#_apgp4mx4xtu5" id="_apgp4mx4xtu5"></a>

#### Delete Certificate Throws Error (150176) <a href="#_roh84vvxlujf" id="_roh84vvxlujf"></a>

#### Rich Text editors fail to load intermittently (150318) <a href="#_frphejrpj5ty" id="_frphejrpj5ty"></a>

#### Question editor not appearing (150571) <a href="#_b67cvh9cy9v" id="_b67cvh9cy9v"></a>

#### Notifications Fail if the instructor feedback author is null or missing (154152) <a href="#_ruttrv8ge5e4" id="_ruttrv8ge5e4"></a>

#### Send Support Message Does not Send (154188) <a href="#_xyc5jfos6hyn" id="_xyc5jfos6hyn"></a>
