CISM Tableau Style Guide

Contents

[Purpose](#purpose)

[When not to use Tableau](#when not to use tableau)

[Style and Design Guidance](#style and design guidance)

[Dashboard Purpose](#dashboard purpose)

[Define Your Purpose at the Start](#define your purpose at the start)

[Data Honesty](#data honesty)

[Basic Dashboard Design](#basic dashboard design)

[Filters](#filters)

[Navigability](#navigability)

[Prepare for printing](#prepare for printing)

[Data Good Practices](#data good practices)

[Worksheet Design](#worksheet design)

[Choosing the Appropriate Graph Type](#choosing the appropriate graph type)

[Colors](#colors)

[Fonts](#fonts)

[Tooltips](#tooltips)

[Worksheet Title Fields](#worksheet title fields)

[Field Formatting](#field formatting)

[Sharing Your Work](#sharing your work)

[Performance Optimizations](#performance optimizations)

[References](#references)

******

<a name="purpose"/>
Purpose
=======

Tableau is a powerful tool for creating a variety of graphs and
dashboards to support business intelligence. While the standard defaults
in Tableau do a good job in guiding an analyst towards making
appropriate design decisions, there are several tips that can be used
and potential pitfalls to avoid to help your visualization be most
effective. This document is an evolving guide to common practices to use
throughout the design, refinement, and publishing process.

When not to use Tableau
-----------------------

For all the power and ease of use of Tableau, there are a number of
situations where Tableau is not the right choice. A key example is the
use of Tableau in place of developing extract-transform-load (ETL)
operations. If Tableau is being used not as a final display mechanism
for your data, but instead getting data from one or more data sources,
performing calculations on that data, and then copying out that data to
Excel or another tool, you should engage with Knowledge Management to
explore other options.

Complex cross-tab reports are also not well suited for Tableau. Any sort
of static broad report with lots of text is a better candidate for
development in a dedicated reporting engine. If you are presenting a
data overview, also consider if a large table of lookup information is
really needed. Often dashboard designs are better with little textual
lookups. 

Tableau workbooks are not full reports. While striving for self-evident
design is a good target, presenting a workbook or dashboard to a request
from a non-technical stakeholder, unless specifically requested, will
confuse rather than add clarity.

<a name="style and desing guidance"/>
Style and Design Guidance
=========================

This section includes guidance on choices to make in use of Tableau. As
guidance, there are instances where deviation from these recommendations
may be necessary. These deviations should be done with caution and only
with careful consideration.

Dashboard Purpose
-----------------

A dashboard is a visual display of the most important information needed
to achieve one or more objectives; consolidated and arranged on a single
screen so the information can be monitored at a glance. – Stephen
Few (Few)

Tableau is actually rather weak on formal dashboard design. The
information dense designs portrayed by Few and other visualization
experts are often very tricky to do in Tableau. In our organization, a
dashboard falls within the Tableau definition which is simply a
collection of more than one visualization on a single pane.

### Define Your Purpose at the Start

Before connecting to data and dragging dimensions and measures around,
have a clear picture of for whom you are designing this visualization.
Is this a draft vis for your own quick understanding of a data set or
will this be the basis of a document to be shared with management or
stakeholders outside of our team? What questions will these users be
bringing to your visualization (what do that want to know)? What actions
do you want to inspire (what do you want them to do with the
information)?

For larger projects, it may be useful to jot down a few quick notes on
the audience, primary questions, and desired outcomes to refer to
throughout your design process.

### Data Honesty

Presenting an unbiased picture of your data is of paramount importance.
Be explicit in defining the limitations of your data (are there missing
elements or other incomplete observations that may influence your data)?
A cover page with key assumptions can go a long way to establishing
trust with your audience, particularly for difficult messages.

<a name="basic dashboard design"/>
Basic Dashboard Design
----------------------

All visualizations should fit within standard resolution without
scrolling or awkward compressions. For visualizations intended for
on-screen interactive display, there may be opportunities where vertical
scrolling is appropriate, but these should be avoided wherever possible.
A dashboard should fit on a single screen with no scrolling. (INSERT
OUR STD SCREEN REZ HERE).

*  Fix the dashboard size to Desktop.

*  Beware of fit entire view - it can mess up your formatting in
unexpected ways. Fit width is generally a safer alternative.

### Filters

*  Filters, if being displayed on screen, may scroll.

*  Dashboards should display elegantly no matter what combination
of items are selected.

*  Filter to include just what you want instead of excluding what
you don’t, to prevent changing data from displaying differently - DLP
group issue

*  If using cascading/hierarchical filters (e.g. Department:
Subdepartment), select 'Show only relevant values').

*  Avoid filtering Dimensions that are placed on the Columns
shelf.

  * Losing control of the width of your sheet can often cause
formatting problems.

### Navigability

*  Worksheets can proliferate over the life of a workbook. If the
number of worksheets or dashboards in a workbook grows large, either:

  * Prune unnecessary worksheets, or

  * If large number of worksheets are needed, consider a front page
with navigation links

*  Once worksheets are added to a dashboard, hide them so they
are not displayed simultaneously with the dashboard when published to
either Reader or Server.

### Prepare for printing

*  Manually set the page orientation to landscape orientation.

*  Captions (Worksheets only): Captions print by default on
worksheets and are automatically populated with a verbose and not very
useful description of the visualization. Either:

  * Turn them off (uncheck File: Page Setup: Show: Captions).

  * Edit the caption to something meaningful for your users.

### Data Good Practices

*  If displaying information that updates periodically, include a
"Data As Of" field data currency.

*  Include the FAQ page designed by Knowledge Management. Even if
the workbook will not be published to Tableau Server, including the FAQ
page on any workbook that is not a throw away session helps provide
trace back of what it was intended to do.

Worksheet Design
----------------

### Choosing the Appropriate Graph Type

*  Pie charts are *never* a good idea. Period.

*  Basic bar and line charts are almost always your best choice.

*  If you have long labels, horizontal bars may be a better
choice than vertical bars.

*  Beware stacked and grouped bar charts.

*  When in doubt, reference the Perceptual Edge Graph Selection
Matrix, found at
[http://www.perceptualedge.com/articles/misc/Graph\_Selection\_Matrix.pdf](http://www.perceptualedge.com/articles/misc/Graph_Selection_Matrix.pdf).

### Colors

*  Watch out for the use of color, it doesn't print well.

*  Use the color blind pallet whenever possible.

*  Don't use more than five colors.

### Fonts

*  Use the default fonts.

*  Indicate emphasis: Only a single text characteristic needs to
be changed. Don't overwhelm the user by changing more than a single
attribute versus surrounding text. For example, good choices such as
**bold**, *italic*, underline, or color as opposed to overly noisy
***bold*** or colorful text.

### Tooltips

*  Edit these to be meaningful for your users.

*  Many visualizations have something that is "Number of records"
but should probably be something else "Number of Users", "patient
count", etc.

### Worksheet Title Fields

The worksheet titles from the tabs automatically populate the title
field which can be optionally displayed/hidden in the worksheet and in
any dashboard which uses those sheets. While the title fields can be
edited manually, this makes later finding of the worksheets that
comprise your dashboard very difficult if the tab is no longer named the
same as the title.

### Field Formatting

*  Percentages should default to no more than one decimal place
of precision. Excessive significant digits are difficult to distinguish
visually. If there is a need for high degrees of precision, a report may
be called for rather than a visualization.

*  Numbers that are integers should never display decimal places
(e.g. 1.0 people).

*  Set formats, sorting, etc. on the dimension itself. This saves
having to redo the formatting on individual sheets).

<a name="sharing your work"/>
Sharing Your Work
-----------------

*  If using a data extract, always distribute your file as a
packaged workbook (.twbx). This avoids extracts from being separated
from the visualization.

*  Be sure to hit escape to deselect all items when publishing.
Tableau will open to the worksheet/dashboard you have open when you
save. Tableau Server will also highlight any currently selected sections
of your dashboard.

*  Publish/Save with the worksheet you want users to start with
open.

*  File Names: Do not put version numbers in your file name when
publishing (users don't need to know your version control
issues/practices).

<a name="performance optimizations"/>
Performance Optimizations
-------------------------

*  Extract only the info you need.

*  Hide unused fields (not during dev.) when ready to publish.

*  Filter data that is not displayed (really old historical).

******

<a name="references"/>
References
==========

Few, Stephen. *Dashboard Confusion Revisited*. n.d.
\<http://www.perceptualedge.com/articles/03-22-07.pdf\>.

Tableau. "Tableau Style Guide." n.d.

—. *Tableau Visual Guidebook*. n.d.
\<http://www.tableausoftware.com/sites/default/files/whitepapers/VisualGuidebookTabRead.pdf\>.

—. "Tableau's Visual Best Practices Document." n.d.

University, Oxford. *Tableau Style Guide*. n.d.
\<https://weblearn.ox.ac.uk/access/content/group/6a4b704f-24ea-4b87-bc8d-bf34327e3979/Tableau%20style%20guide.pdf\>.

 
