# Mac OS X Automator Services
These are some of the Services I have created (you can access them by selecting some text in any application, select the `Services` menu.
Automator Services are found on your Mac under the `~Library/Services` folder.

## Greenhouse
Lookup a person in Greenhouse from the selected text.

    on run {input, parameters}
        set urlloc to "https://app.greenhouse.io/people?job_status=all&sort_by=last_activity&sort_order=desc&type=all&search_terms=" & input
        open location urlloc
        return input
    end run

## LinkedIn
Lookup a person in LinkedIn from the selected text.

    on run {input, parameters}
        set urlloc to "https://www.linkedin.com/search/results/all/?origin=GLOBAL_SEARCH_HEADER&keywords=" & input
        open location urlloc
        return input
    end run
