# agenda_barcelona_sc

Educational scraping project consisting in scraping Barcelona events from Barcelona administration website.

This code scrapes Barcelona's agenda website (https://guia.barcelona.cat/ca) and gets the main information of each event for a specified set of time.

calling the main function:

    scrape_agenda(agenda,ndays,nr,threading = True):

    agenda: dataframe with the columns as the agenda.csv file explained below.
    ndays: integer starting from current date, number of days you want to retrieve the agenda for.
    nr: integer number of events per day
    threading: True concurrency enabled. False otherwise.

    returns: dataframe with the detailed information of each event for the ndays after current date with the same format as agenda

The returned data frame is storead as "agenda.csv" file with the following attributes:

    Event_Name: Title of the event
    Starting_from: Starting date or Permanent event
    Ending: Ending date or "-" if Permanent event or day event
    Location: Venue
    Address: Address of the venue
    Description: Short description of the event
    Link: Link to the specific event page from which you can get more information.

