# Stop Data (January 1, 2023 – June 30, 2024)

This dataset contains detailed records of all stops conducted by the Metropolitan Police Department (MPD) of Washington, D.C., from January 1, 2023, to June 30, 2024.

## Source

- Data Publisher: Metropolitan Police Department (MPD)
- Portal: [https://catalog.data.gov/dataset/stop-data-b6fdf](https://catalog.data.gov/dataset/stop-data-b6fdf)
- Formats: CSV, GeoJSON, Shapefile, KML, ArcGIS REST Services

## Description

Each row in the dataset represents a single person involved in a stop. Multiple individuals stopped in the same incident appear as separate rows.

The dataset includes both ticket-related and investigatory stops, as well as protective pat-downs, property searches, and arrests. Harbor stops and bicycle stops are also included.

## Key Fields

- `stop_id`, `person_id`: Unique identifiers
- `stop_date`, `stop_time`, `stop_duration`
- `stop_type`: Type of stop (ticket, investigatory, etc.)
- `stop_reason_ticket`, `stop_reason_nonticket`, `stop_reason_harbor`
- `search_conducted`, `search_type_person`, `search_type_property`
- `arrest_made`, `ticket_issued`
- `subject_race`, `subject_gender`, `subject_age`
- `stop_location_block`: Location of stop
- `officer_assignment`, `officer_psa`: Officer bureau and district info

## Notes and Limitations

- Many fields contain `NULL` depending on the type of stop.
- A portion of tickets are handwritten and may appear in the dataset with a delay.
- Officer assignment data is based on pay periods prior to July 2023, and stop date afterward.
- Some stops (e.g., harbor or centralized processing stops) may appear outside typical district boundaries.
- The dataset is subject to ongoing review and updates by MPD.

## License

This data is publicly available under open government license terms. Refer to the [catalog listing](https://catalog.data.gov/dataset/stop-data-b6fdf) for more information.

