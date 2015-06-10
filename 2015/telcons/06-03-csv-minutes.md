##TAG teleconf

####27 May 2015


####Present: Dan (dka), Mark (mnot), Alex, David, Yves

####Guests: Jeni Tennison (ODI)

####Regrets: Peter

####Chair: Dan

####Scribe: Dan

####Topic CSV on the Web

--

[Agenda](https://github.com/w3ctag/meetings/blob/gh-pages/2015/telcons/06-03-csv-agenda.md)

Present: Jenit, Dan, Mnot, Yves,dbaron

Topic: URL comparisons when retrieving metadata files - https://github.com/w3c/csvw/issues/562

mnot: .wellknown location stuff … folks working through options on list and on github … any update beyond that?

jenit: the latest suggestion I made was https://lists.w3.org/Archives/Public/www-tag/2015May/0029.html - I suggested having a default file wen that was missing – same behoviour of what we currently have. Allow people to use .well-known file to adjust behavior.

mnot: in terms of the fault - makes me feel a little weird. assumptions of default. if you have early implementions/ deployments that would [be good]

jenit: yes makes sense. we can do that with the test suite – we can do that with the CSV – with an example site that we have. and that we can maintain on github – that would work.

[mnot & jenit: to speak to paul downey.]

jenit: i don't see any reason not to use that link header syntax.

mnot: not the best syntax – it's what has been defied in antiquity. it's there.

jenit: implementation will have to parse it anyway because of the link headers. it means they don't have to repeat anything. Also extensible.

mnot: [yes]

jenit: I will proceed with that. … other issues less important. Planning to get a CR done for the 20th of June.

dka: we'll have to have the rest of the call next week to go through the rest of the feedback....

[some additional discussion on CSV draft https://github.com/w3ctag/spec-reviews/issues/55]

jenit: I thought initially we would end up with a package, but what we've ended up with is CSV files on the web but you can reference between them.

jenit: you can have a group of tables comprised of csv files all over the web.

alex: any examples of uses of this format with javascript – how do I access it?

jenit: you'd need to have a JS implementation of the spec to read in the CSV – one of the specs converts into JSON and that's the closest we have to a JS interface.

alex: no IDL or anything?

jenit: no but if you have recommendations on what that should look like for v.next then I'd be open – not in our charter though.

alex: i'd like to find a way to make this data more easily useful from a web page.

jenit: i'd like to as well.


