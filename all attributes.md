# intro
This is based on the response of API call `1. Get a list of attribute names`
`https://www.movebank.org/movebank/service/direct-read?attributes`

Some of the attributes are not covered in API document. It took me some trials and errors to get some calls right, so I will add note here.
- all `entity-type= ...` need to be written as `entity_type= ...`, change `-` to `_`
- some call only need one parameter of `entity_type`, some will need to add `study_id`, some will need `tag_study_id` instead of `study_id`, some will need to add `sensor_type_id`

The response sections are reordered for better lookup. Notes will be written in quote format

> note:

# annotated response
Specify one of the following entity types: deployment, event, individual, sensor, study, study_attribute, tag, tag_type, taxon
Optional parameter: header-format=underscore
When connecting via https you must specify the parameters user=... and password=...
Specify output attributes and filter conditions depending on the entity type.

## entity-type=deployment
Output attributes: access_profile_id, animal_life_stage, animal_mass, animal_reproductive_condition, attachment_type, behavior_according_to, comments, data_processing_software, deploy_off_latitude, deploy_off_longitude, deploy_off_person, deploy_off_timestamp, deploy_on_latitude, deploy_on_longitude, deploy_on_person, deploy_on_timestamp, deployment_end_comments, deployment_end_type, duty_cycle, external_id, external_id_namespace_id, geolocator_calibration, geolocator_light_threshold, geolocator_sensor_comments, geolocator_sun_elevation_angle, habitat_according_to, i_am_owner, id, individual_id, local_identifier, location_accuracy_comments, manipulation_comments, manipulation_type, partial_identifier, study_id, study_site, tag_id, tag_readout_method
Filter attributes: access_profile_id, animal_life_stage, animal_mass, animal_reproductive_condition, attachment_type, behavior_according_to, comments, data_processing_software, deploy_off_latitude, deploy_off_longitude, deploy_off_person, deploy_off_timestamp, deploy_on_latitude, deploy_on_longitude, deploy_on_person, deploy_on_timestamp, deployment_end_comments, deployment_end_type, duty_cycle, external_id, external_id_namespace_id, geolocator_calibration, geolocator_light_threshold, geolocator_sensor_comments, geolocator_sun_elevation_angle, habitat_according_to, i_am_owner, id, individual_id, local_identifier, location_accuracy_comments, manipulation_comments, manipulation_type, partial_identifier, study_id, study_site, tag_id, tag_readout_method

> example: call with `study_id`
> `https://www.movebank.org/movebank/service/direct-read?entity_type=deployment&study_id=1764627`

```
|animal_life_stage |animal_mass |animal_reproductive_condition |attachment_type |behavior_according_to |comments                |data_processing_software |deploy_off_latitude |deploy_off_longitude |deploy_off_person |deploy_off_timestamp    |deploy_on_latitude |deploy_on_longitude |deploy_on_person |deploy_on_timestamp     |deployment_end_comments         |deployment_end_type |duty_cycle   |geolocator_calibration |geolocator_light_threshold |geolocator_sensor_comments |geolocator_sun_elevation_angle |habitat_according_to |        id|local_identifier |location_accuracy_comments |manipulation_comments |manipulation_type |partial_identifier |study_site           |tag_readout_method |
|:-----------------|:-----------|:-----------------------------|:---------------|:---------------------|:-----------------------|:------------------------|:-------------------|:--------------------|:-----------------|:-----------------------|:------------------|:-------------------|:----------------|:-----------------------|:-------------------------------|:-------------------|:------------|:----------------------|:--------------------------|:--------------------------|:------------------------------|:--------------------|---------:|:----------------|:--------------------------|:---------------------|:-----------------|:------------------|:--------------------|:------------------|
|5-8 years old     |            |                              |collar          |                      |                        |                         |                    |                     |                  |2005-12-08 23:59:59.000 |                   |                    |                 |2005-07-14 00:00:00.000 |                                |                    |hourly fixes |                       |                           |                           |                               |                     | 198016104|T12-Cilla        |                           |                      |none              |                   |Kruger National Park |                   |
|10-12 years old   |            |                              |collar          |                      |used in Getz et al 2007 |                         |                    |                     |                  |2005-10-29 23:59:59.000 |                   |                    |                 |2005-07-15 00:00:00.000 |collar failed before 2006-03-07 |equipment-failure   |hourly fixes |                       |                           |                           |                               |                     | 198016098|T13-Mvubu        |                           |                      |none              |                   |Kruger National Park |                   |
|8-12 years old    |            |                              |collar          |                      |used in Getz et al 2007 |                         |                    |                     |                  |2006-02-16 23:59:59.000 |                   |                    |                 |2005-09-16 00:00:00.000 |                                |                    |hourly fixes |                       |                           |                           |                               |                     | 198016106|T15-Pepper       |                           |                      |none              |                   |Kruger National Park |                   |
|8-12 years old    |            |                              |collar          |                      |used in Getz et al 2007 |                         |                    |                     |                  |2005-10-08 23:59:59.000 |                   |                    |                 |2005-07-27 00:00:00.000 |collar failed                   |equipment-failure   |hourly fixes |                       |                           |                           |                               |                     | 198016103|T16-Gabs         |                           |                      |none              |                   |Kruger National Park |                   |
|8-12 years old    |            |                              |collar          |                      |                        |                         |                    |                     |                  |2006-12-31 23:59:59.000 |                   |                    |                 |2006-04-25 00:00:00.000 |                                |                    |hourly fixes |                       |                           |                           |                               |                     | 198016105|T17-Pepper       |                           |                      |none              |                   |Kruger National Park |                   |
|5-8 years old     |            |                              |collar          |                      |                        |                         |                    |                     |                  |2006-04-23 23:59:59.000 |                   |                    |                 |2005-08-23 00:00:00.000 |                                |                    |hourly fixes |                       |                           |                           |                               |                     | 198016101|T17-Toni         |                           |                      |none              |                   |Kruger National Park |                   |
|8-12 years old    |            |                              |collar          |                      |                        |                         |                    |                     |                  |2005-06-27 23:59:59.000 |                   |                    |                 |2005-04-05 00:00:00.000 |                                |                    |hourly fixes |                       |                           |                           |                               |                     | 198016100|T7-Gabs          |                           |                      |none              |                   |Kruger National Park |                   |
|8-12 years old    |            |                              |collar          |                      |used in Getz et al 2007 |                         |                    |                     |                  |2006-05-26 23:59:59.000 |                   |                    |                 |2005-09-15 00:00:00.000 |                                |                    |hourly fixes |                       |                           |                           |                               |                     | 198016102|T7-Queen         |                           |                      |none              |                   |Kruger National Park |                   |
|8-12 years old    |            |                              |collar          |                      |                        |                         |                    |                     |                  |2005-06-02 23:59:59.000 |                   |                    |                 |2005-02-17 00:00:00.000 |                                |                    |hourly fixes |                       |                           |                           |                               |                     | 198016099|T8-Queen         |                           |                      |none              |                   |Kruger National Park |                   |
```

## entity-type=event
Output attributes: acceleration_axes, acceleration_raw_x, acceleration_raw_y, acceleration_raw_z, acceleration_sampling_frequency_per_axis, acceleration_x, acceleration_y, acceleration_z, accelerations_raw, activity_count, activity_count, algorithm_marked_outlier, argos_altitude, argos_best_level, argos_calcul_freq, argos_error_radius, argos_gdop, argos_iq, argos_lat1, argos_lat2, argos_lc, argos_lon1, argos_lon2, argos_nb_mes, argos_nb_mes_120, argos_nb_mes_identical, argos_nopc, argos_orientation, argos_pass_duration, argos_sat_id, argos_semi_major, argos_semi_minor, argos_sensor_1, argos_sensor_2, argos_sensor_3, argos_sensor_4, argos_transmission_timestamp, argos_valid_location_algorithm, argos_valid_location_manual, barometric_depth, barometric_height, barometric_pressure, bas_compensated_latitute, bas_confidence, bas_fix_type, bas_mid_value_secs, bas_stationary_latitute, bas_transition_1, bas_transition_2, battery_charge_percent, battery_charging_current, behavioural_classification, comments, compass_heading, deployment_id, eobs_acceleration_axes, eobs_acceleration_sampling_frequency_per_axis, eobs_accelerations_raw, eobs_activity, eobs_activity_samples, eobs_battery_voltage, eobs_fix_battery_voltage, eobs_horizontal_accuracy_estimate, eobs_key_bin_checksum, eobs_speed_accuracy_estimate, eobs_start_timestamp, eobs_status, eobs_temperature, eobs_type_of_fix, eobs_used_time_to_get_fix, event_id, event_set_id, external_temperature, flt_switch, gps_dop, gps_fix_type, gps_hdop, gps_maximum_signal_strength, gps_satellite_count, gps_time_to_fix, gps_vdop, ground_speed, gsm_mcc_mnc, gsm_signal_strength, gt_activity_count, gt_sys_week, gt_tx_count, habitat, heading, height_above_ellipsoid, height_above_msl, height_raw, individual_id, internal_temperature, light_level, location_error_numerical, location_error_percentile, location_error_text, location_lat, location_long, magnetic_field_raw_x, magnetic_field_raw_y, magnetic_field_raw_z, manually_marked_outlier, manually_marked_valid, migration_stage, migration_stage_standard, modelled, mw_activity_count, mw_show_in_kml, ornitela_transmission_protocol, proofed, raptor_workshop_behaviour, raptor_workshop_deployment_special_event, raptor_workshop_migration_state, sensor_type_id, study_id, study_specific_measurement, tag_battery_voltage, tag_id, tag_tech_spec, tag_voltage, technosmart_activity, technosmart_signal_quality, tilt_angle, tilt_x, tilt_y, tilt_z, timestamp, transmission_timestamp, underwater_count, underwater_time, vertical_error_numerical, visible, waterbird_workshop_behaviour, waterbird_workshop_deployment_special_event, waterbird_workshop_migration_state
Filter attributes: acceleration_axes, acceleration_raw_x, acceleration_raw_y, acceleration_raw_z, acceleration_sampling_frequency_per_axis, acceleration_x, acceleration_y, acceleration_z, accelerations_raw, activity_count, activity_count, algorithm_marked_outlier, argos_altitude, argos_best_level, argos_calcul_freq, argos_error_radius, argos_gdop, argos_iq, argos_lat1, argos_lat2, argos_lc, argos_lon1, argos_lon2, argos_nb_mes, argos_nb_mes_120, argos_nb_mes_identical, argos_nopc, argos_orientation, argos_pass_duration, argos_sat_id, argos_semi_major, argos_semi_minor, argos_sensor_1, argos_sensor_2, argos_sensor_3, argos_sensor_4, argos_transmission_timestamp, argos_valid_location_algorithm, argos_valid_location_manual, barometric_depth, barometric_height, barometric_pressure, bas_compensated_latitute, bas_confidence, bas_fix_type, bas_mid_value_secs, bas_stationary_latitute, bas_transition_1, bas_transition_2, battery_charge_percent, battery_charging_current, behavioural_classification, comments, compass_heading, deployment_id, eobs_acceleration_axes, eobs_acceleration_sampling_frequency_per_axis, eobs_accelerations_raw, eobs_activity, eobs_activity_samples, eobs_battery_voltage, eobs_fix_battery_voltage, eobs_horizontal_accuracy_estimate, eobs_key_bin_checksum, eobs_speed_accuracy_estimate, eobs_start_timestamp, eobs_status, eobs_temperature, eobs_type_of_fix, eobs_used_time_to_get_fix, event_id, event_set_id, external_temperature, flt_switch, gps_dop, gps_fix_type, gps_hdop, gps_maximum_signal_strength, gps_satellite_count, gps_time_to_fix, gps_vdop, ground_speed, gsm_mcc_mnc, gsm_signal_strength, gt_activity_count, gt_sys_week, gt_tx_count, habitat, heading, height_above_ellipsoid, height_above_msl, height_raw, individual_id, internal_temperature, light_level, location_error_numerical, location_error_percentile, location_error_text, location_lat, location_long, magnetic_field_raw_x, magnetic_field_raw_y, magnetic_field_raw_z, manually_marked_outlier, manually_marked_valid, migration_stage, migration_stage_standard, modelled, mw_activity_count, mw_show_in_kml, ornitela_transmission_protocol, proofed, raptor_workshop_behaviour, raptor_workshop_deployment_special_event, raptor_workshop_migration_state, sensor_type_id, study_id, study_specific_measurement, tag_battery_voltage, tag_id, tag_tech_spec, tag_voltage, technosmart_activity, technosmart_signal_quality, tilt_angle, tilt_x, tilt_y, tilt_z, timestamp, transmission_timestamp, underwater_count, underwater_time, vertical_error_numerical, visible, waterbird_workshop_behaviour, waterbird_workshop_deployment_special_event, waterbird_workshop_migration_state

> by default only core columns are returned
> `https://www.movebank.org/movebank/service/direct-read?entity_type=event&study_id=2911040`
> to add more attributes, need to know what are available first. use `study_attribute` to find out.


## entity-type=individual
Output attributes: access_profile_id, comments, death_comments, default_profile_eventdata_id, earliest_date_born, exact_date_of_birth, external_id, external_id_namespace_id, i_am_owner, id, latest_date_born, local_identifier, ring_id, sex, study_id, taxon_canonical_name, taxon_id
Filter attributes: access_profile_id, comments, death_comments, default_profile_eventdata_id, earliest_date_born, exact_date_of_birth, external_id, external_id_namespace_id, i_am_owner, id, latest_date_born, local_identifier, ring_id, sex, study_id, taxon_canonical_name, taxon_id

> example. The `id` - `local_identifier` information could be important
> `https://www.movebank.org/movebank/service/direct-read?entity_type=individual&study_id=1764627`

```
|comments |death_comments |earliest_date_born |exact_date_of_birth |      id|latest_date_born |local_identifier |ring_id |sex |taxon_canonical_name |
|:--------|:--------------|:------------------|:-------------------|-------:|:----------------|:----------------|:-------|:---|:--------------------|
|         |               |                   |                    | 1764825|                 |Cilla            |        |f   |                     |
|         |               |                   |                    | 1764822|                 |Gabs             |        |f   |                     |
|         |               |                   |                    | 1764828|                 |Mvubu            |        |f   |                     |
|         |               |                   |                    | 1764834|                 |Pepper           |        |f   |                     |
|         |               |                   |                    | 1764819|                 |Queen            |        |f   |                     |
|         |               |                   |                    | 1764831|                 |Toni             |        |f   |                     |
```

## entity-type=sensor
Output attributes: external_id, external_id_namespace_id, id, manufacturer_name, model, sensor_type_id, tag_id, tag_study_id
Filter attributes: external_id, external_id_namespace_id, id, manufacturer_name, model, sensor_type_id, tag_id, tag_study_id

> note you need to specify the study with **tag_study_id** instead of `study_id`
> `https://www.movebank.org/movebank/service/direct-read?entity_type=sensor&tag_study_id=1764627`

```
|        id| sensor_type_id|    tag_id|
|---------:|--------------:|---------:|
| 197990563|            653| 197990562|
| 197990567|            653| 197990566|
| 197990569|            653| 197990568|
| 197990571|            653| 197990570|
| 197990573|            653| 197990572|
| 197990575|            653| 197990574|
| 197990577|            653| 197990576|
```


## entity-type=study
Output attributes: access_profile_download_id, access_profile_id, acknowledgements, bounding_box, citation, comments, contact_person_id, default_profile_eventdata_id, default_profile_refdata_id, external_id, external_id_namespace_id, grants_used, has_quota, i_am_owner, i_can_see_data, id, license_terms, location_description, main_location_lat, main_location_long, name, number_of_deployments, number_of_events, number_of_individuals, number_of_tags, principal_investigator_address, principal_investigator_email, principal_investigator_id, principal_investigator_name, study_id, study_objective, study_type, suspend_license_terms, there_are_data_which_i_cannot_see, timestamp_end, timestamp_start
Filter attributes: access_profile_download_id, access_profile_id, acknowledgements, bounding_box, citation, comments, contact_person_id, default_profile_eventdata_id, default_profile_refdata_id, external_id, external_id_namespace_id, grants_used, has_quota, i_am_owner, id, license_terms, location_description, main_location_lat, main_location_long, name, number_of_deployments, number_of_events, number_of_individuals, number_of_tags, principal_investigator_address, principal_investigator_email, principal_investigator_id, principal_investigator_name, study_id, study_objective, study_type, suspend_license_terms, timestamp_end, timestamp_start

> covered in API document

## entity-type=study_attribute
Output attributes: data_type, sensor_type_id, short_name, study_id
Filter attributes: data_type, sensor_type_id, short_name, study_id

Example query string: ?entity-type=individual&study=80355,80725&attributes=id,local-identifier,taxon

> Need `study_id` and `sensor_type_id` in call. Get `sensor_type_id` from `sensor` call.
> `https://www.movebank.org/movebank/service/direct-read?entity_type=study_attribute&study_id=1764627&sensor_type_id=653`

```
| study_id| sensor_type_id|short_name               |data_type |
|--------:|--------------:|:------------------------|:---------|
|  1764627|            653|algorithm_marked_outlier |boolean   |
|  1764627|            653|external_temperature     |decimal   |
|  1764627|            653|location_lat             |decimal   |
|  1764627|            653|location_long            |decimal   |
|  1764627|            653|manually_marked_outlier  |boolean   |
|  1764627|            653|timestamp                |datetime  |
|  1764627|            653|visible                  |boolean   |
```

## entity-type=tag
Output attributes: access_profile_id, beacon_frequency, comments, external_id, external_id_namespace_id, i_am_owner, id, local_identifier, manufacturer_name, model, processing_type, serial_no, study_id, tag_failure_comments, tag_production_date, tag_type_id, weight
Filter attributes: access_profile_id, beacon_frequency, comments, external_id, external_id_namespace_id, i_am_owner, id, local_identifier, manufacturer_name, model, processing_type, serial_no, study_id, tag_failure_comments, tag_production_date, tag_type_id, weight

> We need `study_id` here.
> `https://www.movebank.org/movebank/service/direct-read?entity_type=tag&study_id=1764627`

```
|beacon_frequency |comments |        id|local_identifier |manufacturer_name        |model |processing_type |serial_no |tag_failure_comments |tag_production_date |weight |
|:----------------|:--------|---------:|:----------------|:------------------------|:-----|:---------------|:---------|:--------------------|:-------------------|:------|
|                 |         | 197990562|T8               |Africa Wildlife Tracking |      |                |          |                     |                    |       |
|                 |         | 197990566|T7               |Africa Wildlife Tracking |      |                |          |                     |                    |       |
|                 |         | 197990568|T12              |Africa Wildlife Tracking |      |                |          |                     |                    |       |
|                 |         | 197990570|T13              |Africa Wildlife Tracking |      |                |          |                     |                    |       |
|                 |         | 197990572|T16              |Africa Wildlife Tracking |      |                |          |                     |                    |       |
|                 |         | 197990574|T17              |Africa Wildlife Tracking |      |                |          |                     |                    |       |
|                 |         | 197990576|T15              |Africa Wildlife Tracking |      |                |          |                     |                    |       |
```

## entity-type=tag_type
Output attributes: description, external_id, external_id_namespace_id, id, is_location_sensor, name
Filter attributes: description, external_id, external_id_namespace_id, id, is_location_sensor, name

> Many data download will use the sensor id in data, so you will need the table from this inquiry to map the id to sensor name, types etc.
> `https://www.movebank.org/movebank/service/direct-read?entity_type=tag_type`

```
|description |external_id            |       id|is_location_sensor |name                   |
|:-----------|:----------------------|--------:|:------------------|:----------------------|
|            |bird-ring              |      397|true               |Bird Ring              |
|            |gps                    |      653|true               |GPS                    |
|            |radio-transmitter      |      673|true               |Radio Transmitter      |
|            |argos-doppler-shift    |    82798|true               |Argos Doppler Shift    |
|            |natural-mark           |  2365682|true               |Natural Mark           |
|            |acceleration           |  2365683|false              |Acceleration           |
|            |solar-geolocator       |  3886361|true               |Solar Geolocator       |
|            |accessory-measurements |  7842954|false              |Accessory Measurements |
|            |solar-geolocator-raw   |  9301403|false              |Solar Geolocator Raw   |
|            |barometer              | 77740391|false              |Barometer              |
|            |magnetometer           | 77740402|false              |Magnetometer           |
```

## entity-type=taxon
Output attributes: author_string, canonical_name, external_id, external_id_namespace_id, hierarchy_string, id, name_1, name_2, name_3, parent_taxon_id, valid
Filter attributes: author_string, canonical_name, external_id, external_id_namespace_id, hierarchy_string, id, name_1, name_2, name_3, parent_taxon_id, valid

> This will return a 8M table of all taxon names
> `https://www.movebank.org/movebank/service/direct-read?entity_type=taxon`

```
|author_string              |canonical_name             |external_id |hierarchy_string                        |  id|name_1          |name_2          |name_3 |valid |
|:--------------------------|:--------------------------|:-----------|:---------------------------------------|---:|:---------------|:---------------|:------|:-----|
|                           |Chordata                   |            |16762-817                               | 817|Chordata        |                |       |      |
|                           |Ascidiacea                 |            |16762-817-16763-818                     | 818|Ascidiacea      |                |       |      |
|                           |Enterogona                 |            |16762-817-16763-818-819                 | 819|Enterogona      |                |       |      |
|Lahille, 1887              |Aplousobranchia            |            |16762-817-16763-818-819-820             | 820|Aplousobranchia |                |       |      |
|Forbes and Hanley, 1848    |Clavelinidae               |            |16762-817-16763-818-819-820-821         | 821|Clavelinidae    |                |       |      |
|                           |Cystodytes                 |            |16762-817-16763-818-819-820-821-822     | 822|Cystodytes      |                |       |      |
|                           |Cystodytes lobatus         |            |16762-817-16763-818-819-820-821-822-823 | 823|Cystodytes      |lobatus         |       |      |
|(Della Valle, 1877)        |Cystodytes dellechiajei    |            |16762-817-16763-818-819-820-821-822-824 | 824|Cystodytes      |dellechiajei    |       |      |
|Sluiter, 1914              |Cystodytes antarcticus     |            |16762-817-16763-818-819-820-821-822-825 | 825|Cystodytes      |antarcticus     |       |      |
|Savigny, 1816              |Clavelina                  |            |16762-817-16763-818-819-820-821-826     | 826|Clavelina       |                |       |      |
|Van Name, 1931             |Clavelina huntsmani        |            |16762-817-16763-818-819-820-821-826-827 | 827|Clavelina       |huntsmani       |       |      |
|                           |Clavelina nana             |            |16762-817-16763-818-819-820-821-826-828 | 828|Clavelina       |nana            |       |      |
|                           |Clavelina lepadiformis     |            |16762-817-16763-818-819-820-821-826-829 | 829|Clavelina       |lepadiformis    |       |      |
|Herdmann, 1880             |Clavelina oblonga          |            |16762-817-16763-818-819-820-821-826-830 | 830|Clavelina       |oblonga         |       |      |
|Van Name, 1921             |Clavelina gigantea         |            |16762-817-16763-818-819-820-821-826-831 | 831|Clavelina       |gigantea        |       |      |
|(Verrill, 1900)            |Clavelina picta            |            |16762-817-16763-818-819-820-821-826-832 | 832|Clavelina       |picta           |       |      |
|Van Name, 1945             |Clavelina fasciculata      |            |16762-817-16763-818-819-820-821-826-833 | 833|Clavelina       |fasciculata     |       |      |
|Della Valle, 1881          |Distaplia                  |            |16762-817-16763-818-819-820-821-834     | 834|Distaplia       |                |       |      |
|Bancroft, 1899             |Distaplia occidentalis     |            |16762-817-16763-818-819-820-821-834-835 | 835|Distaplia       |occidentalis    |       |      |
|                           |Distaplia smithi           |            |16762-817-16763-818-819-820-821-834-836 | 836|Distaplia       |smithi          |       |      |
|                           |Distaplia rosea            |            |16762-817-16763-818-819-820-821-834-837 | 837|Distaplia       |rosea           |       |      |
|Van Name, 1902             |Distaplia bermudensis      |            |16762-817-16763-818-819-820-821-834-838 | 838|Distaplia       |bermudensis     |       |      |
|                           |Distaplia garstangi        |            |16762-817-16763-818-819-820-821-834-839 | 839|Distaplia       |garstangi       |       |      |
|(Sars, 1851)               |Distaplia clavata          |            |16762-817-16763-818-819-820-821-834-840 | 840|Distaplia       |clavata         |       |      |
|(Kowalevsky, 1874)         |Distaplia stylifera        |            |16762-817-16763-818-819-820-821-834-841 | 841|Distaplia       |stylifera       |       |      |
|Sluiter, 1932              |Distaplia colligans        |            |16762-817-16763-818-819-820-821-834-842 | 842|Distaplia       |colligans       |       |      |
|                           |Archidistoma               |            |16762-817-16763-818-819-820-821-843     | 843|Archidistoma    |                |       |      |
|                           |Archidistoma ritteri       |            |16762-817-16763-818-819-820-821-843-844 | 844|Archidistoma    |ritteri         |       |      |
|                           |Archidistoma diaphanes     |            |16762-817-16763-818-819-820-821-843-845 | 845|Archidistoma    |diaphanes       |       |      |
|(Ritter, 1900)             |Archidistoma molle         |            |16762-817-16763-818-819-820-821-843-846 | 846|Archidistoma    |molle           |       |      |
|                           |Archidistoma psammion      |            |16762-817-16763-818-819-820-821-843-847 | 847|Archidistoma    |psammion        |       |      |
|Garstang, 1891             |Archidistoma aggregatum    |            |16762-817-16763-818-819-820-821-843-848 | 848|Archidistoma    |aggregatum      |       |      |
|                           |Pycnoclavella              |            |16762-817-16763-818-819-820-821-849     | 849|Pycnoclavella   |                |       |      |
|                           |Pycnoclavella stanleyi     |            |16762-817-16763-818-819-820-821-849-850 | 850|Pycnoclavella   |stanleyi        |       |      |
|                           |Pycnoclavella aurilucens   |            |16762-817-16763-818-819-820-821-849-851 | 851|Pycnoclavella   |aurilucens      |       |      |
|                           |Polycitor                  |            |16762-817-16763-818-819-820-821-852     | 852|Polycitor       |                |       |      |
|                           |Polycitor searli           |            |16762-817-16763-818-819-820-821-852-853 | 853|Polycitor       |searli          |       |      |
|(Sars, 1851)               |Polycitor vitreus          |            |16762-817-16763-818-819-820-821-852-854 | 854|Polycitor       |vitreus         |       |      |
|(Michaelsen, 1907)         |Polycitor magalhaensis     |            |16762-817-16763-818-819-820-821-852-855 | 855|Polycitor       |magalhaensis    |       |      |
|(Sluiter, 1906)            |Polycitor glareosus        |            |16762-817-16763-818-819-820-821-852-856 | 856|Polycitor       |glareosus       |       |      |
|Caullery, 1909             |Eudistoma                  |            |16762-817-16763-818-819-820-821-857     | 857|Eudistoma       |                |       |      |
|Van Name, 1945             |Eudistoma carolinense      |            |16762-817-16763-818-819-820-821-857-858 | 858|Eudistoma       |carolinense     |       |      |
|(Van Name, 1902)           |Eudistoma olivaceum        |            |16762-817-16763-818-819-820-821-857-859 | 859|Eudistoma       |olivaceum       |       |      |
|(Van Name, 1902)           |Eudistoma capsulatum       |            |16762-817-16763-818-819-820-821-857-860 | 860|Eudistoma       |capsulatum      |       |      |
|(Van Name, 1921)           |Eudistoma hepaticum        |            |16762-817-16763-818-819-820-821-857-861 | 861|Eudistoma       |hepaticum       |       |      |
|(Van Name, 1902)           |Eudistoma obscuratum       |            |16762-817-16763-818-819-820-821-857-862 | 862|Eudistoma       |obscuratum      |       |      |
|Van Name, 1945             |Eudistoma tarponense       |            |16762-817-16763-818-819-820-821-857-863 | 863|Eudistoma       |tarponense      |       |      |
|(Van Name, 1945)           |Eudistoma clarum           |            |16762-817-16763-818-819-820-821-857-864 | 864|Eudistoma       |clarum          |       |      |
|Van Name, 1945)            |Eudistoma platense         |            |16762-817-16763-818-819-820-821-857-865 | 865|Eudistoma       |platense        |       |      |
|Van Name, 1945)            |Eudistoma pachecae         |            |16762-817-16763-818-819-820-821-857-866 | 866|Eudistoma       |pachecae        |       |      |
|Van Name, 1945)            |Eudistoma mexicanum        |            |16762-817-16763-818-819-820-821-857-867 | 867|Eudistoma       |mexicanum       |       |      |
|Van Name, 1945)            |Eudistoma ritteri          |            |16762-817-16763-818-819-820-821-857-868 | 868|Eudistoma       |ritteri         |       |      |
|(Lesson, 1830)             |Distaplia cylindrica       |            |16762-817-16763-818-819-820-821-834-869 | 869|Distaplia       |cylindrica      |       |      |
|Lesson, 1830               |Sycozoa                    |            |16762-817-16763-818-819-820-821-870     | 870|Sycozoa         |                |       |      |
|(Herdman, 1886)            |Sycozoa gaimardi           |            |16762-817-16763-818-819-820-821-870-871 | 871|Sycozoa         |gaimardi        |       |      |
|Lesson, 1830               |Sycozoa sigillinoides      |            |16762-817-16763-818-819-820-821-870-872 | 872|Sycozoa         |sigillinoides   |       |      |
|(Michaelsen, 1898)         |Sycozoa umbellata          |            |16762-817-16763-818-819-820-821-870-873 | 873|Sycozoa         |umbellata       |       |      |
|(Michaelsen, 1907)         |Sycozoa georgiana          |            |16762-817-16763-818-819-820-821-870-874 | 874|Sycozoa         |georgiana       |       |      |
|Milne-Edwards, 1841        |Polyclinidae               |            |16762-817-16763-818-819-820-875         | 875|Polyclinidae    |                |       |      |
|Hartmeyer, 1903            |Aplidium spitzbergense     |            |16762-817-16763-818-819-820-875-919-876 | 876|Aplidium        |spitzbergense   |       |      |
|(Ritter and Forsyth, 1917) |Aplidium californicum      |            |16762-817-16763-818-819-820-875-919-877 | 877|Aplidium        |californicum    |       |      |
|(Ritter and Forsyth, 1917) |Aplidium solidum           |            |16762-817-16763-818-819-820-875-919-878 | 878|Aplidium        |solidum         |       |      |
|(Verrill, 1871)            |Aplidium constellatum      |            |16762-817-16763-818-819-820-875-919-879 | 879|Aplidium        |constellatum    |       |      |
|(Van Name, 1945)           |Aplidium arenatum          |            |16762-817-16763-818-819-820-875-919-880 | 880|Aplidium        |arenatum        |       |      |
|(Van Name, 1945)           |Aplidium propinquum        |            |16762-817-16763-818-819-820-875-919-881 | 881|Aplidium        |propinquum      |       |      |
|(Van Name, 1902)           |Aplidium bermudae          |            |16762-817-16763-818-819-820-875-919-882 | 882|Aplidium        |bermudae        |       |      |
|(Leidy, 1885)              |Aplidium pellucidum        |            |16762-817-16763-818-819-820-875-919-883 | 883|Aplidium        |pellucidum      |       |      |
|(Verrill, 1871)            |Aplidium stellatum         |            |16762-817-16763-818-819-820-875-919-884 | 884|Aplidium        |stellatum       |       |      |
|Savigny, 1816              |Aplidium lobatum           |            |16762-817-16763-818-819-820-875-919-885 | 885|Aplidium        |lobatum         |       |      |
|Cunningham, 1871           |Aplidium fuegiense         |            |16762-817-16763-818-819-820-875-919-886 | 886|Aplidium        |fuegiense       |       |      |
|(Sluiter, 1906)            |Aplidium ordinatum         |            |16762-817-16763-818-819-820-875-919-887 | 887|Aplidium        |ordinatum       |       |      |
|Phipps, 1774               |Synoicum                   |            |16762-817-16763-818-819-820-875-888     | 888|Synoicum        |                |       |      |
|(Ellis and Solander, 1786) |Synoicum pulmonaria        |            |16762-817-16763-818-819-820-875-888-889 | 889|Synoicum        |pulmonaria      |       |      |
|Ritter, 1899               |Synoicum irregulare        |            |16762-817-16763-818-819-820-875-888-890 | 890|Synoicum        |irregulare      |       |      |
|(Ritter, 1899)             |Synoicum jordani           |            |16762-817-16763-818-819-820-875-888-891 | 891|Synoicum        |jordani         |       |      |
|                           |Synoicum kincaidi          |            |16762-817-16763-818-819-820-875-888-892 | 892|Synoicum        |kincaidi        |       |      |
|Redikorzev, 1927           |Synoicum cymosum           |            |16762-817-16763-818-819-820-875-888-893 | 893|Synoicum        |cymosum         |       |      |
|(Ritter and Forsyth, 1917) |Synoicum parfustis         |            |16762-817-16763-818-819-820-875-888-894 | 894|Synoicum        |parfustis       |       |      |
|(Herdman, 1886)            |Synoicum molle             |            |16762-817-16763-818-819-820-875-888-895 | 895|Synoicum        |molle           |       |      |
|(Herdman, 1902)            |Synoicum adareanum         |            |16762-817-16763-818-819-820-875-888-896 | 896|Synoicum        |adareanum       |       |      |
|(Sluiter, 1906)            |Synoicum triplex           |            |16762-817-16763-818-819-820-875-888-897 | 897|Synoicum        |triplex         |       |      |
|(Sluiter, 1912)            |Synoicum pererratum        |            |16762-817-16763-818-819-820-875-888-898 | 898|Synoicum        |pererratum      |       |      |
|(Ritter and Forsyth, 1917) |Synoicum pellucidum        |            |16762-817-16763-818-819-820-875-888-899 | 899|Synoicum        |pellucidum      |       |      |
|(Ritter, 1899)             |Synoicum kinkaidi          |            |16762-817-16763-818-819-820-875-888-900 | 900|Synoicum        |kinkaidi        |       |      |
|Lahille, 1890              |Aplidiopsis                |            |16762-817-16763-818-819-820-875-901     | 901|Aplidiopsis     |                |       |      |
|(Ritter, 1899)             |Aplidiopsis pannosum       |            |16762-817-16763-818-819-820-875-901-902 | 902|Aplidiopsis     |pannosum        |       |      |
|Savigny, 1816              |Polyclinum                 |            |16762-817-16763-818-819-820-875-903     | 903|Polyclinum      |                |       |      |
|(Ritter and Forsyth, 1917) |Polyclinum planum          |            |16762-817-16763-818-819-820-875-903-904 | 904|Polyclinum      |planum          |       |      |
|Van Name, 1945             |Polyclinum laxum           |            |16762-817-16763-818-819-820-875-903-905 | 905|Polyclinum      |laxum           |       |      |
|                           |Polyclinum aurantium       |            |16762-817-16763-818-819-820-875-903-906 | 906|Polyclinum      |aurantium       |       |      |
|Savigny, 1816              |Polyclinum constellatum    |            |16762-817-16763-818-819-820-875-903-907 | 907|Polyclinum      |constellatum    |       |      |
|                           |Ritterella                 |            |16762-817-16763-818-819-820-875-908     | 908|Ritterella      |                |       |      |
|(Oka, 1933)                |Ritterella pulchra         |            |16762-817-16763-818-819-820-875-908-909 | 909|Ritterella      |pulchra         |       |      |
|(Ritter and Forsyth, 1917) |Ritterella aequalisiphonis |            |16762-817-16763-818-819-820-875-908-910 | 910|Ritterella      |aequalisiphonis |       |      |
|Abbott and Trason, 1968    |Ritterella rubra           |            |16762-817-16763-818-819-820-875-908-911 | 911|Ritterella      |rubra           |       |      |
|Ritter, 1904               |Euherdmania                |            |16762-817-16763-818-819-820-875-912     | 912|Euherdmania     |                |       |      |
|(Ritter, 1903)             |Euherdmania claviformis    |            |16762-817-16763-818-819-820-875-912-913 | 913|Euherdmania     |claviformis     |       |      |
|                           |Sidnyum                    |            |16762-817-16763-818-819-820-875-914     | 914|Sidnyum         |                |       |      |
|                           |Sidnyum elegans            |            |16762-817-16763-818-819-820-875-914-915 | 915|Sidnyum         |elegans         |       |      |
|                           |Sidnyum turbinatum         |            |16762-817-16763-818-819-820-875-914-916 | 916|Sidnyum         |turbinatum      |       |      |
|                           |Morchellium                |            |16762-817-16763-818-819-820-875-917     | 917|Morchellium     |                |       |      |
|                           |Morchellium argus          |            |16762-817-16763-818-819-820-875-917-918 | 918|Morchellium     |argus           |       |      |
|Savigny, 1816              |Aplidium                   |            |16762-817-16763-818-819-820-875-919     | 919|Aplidium        |                |       |      |
|(Verrill, 1871)            |Aplidium pallidum          |            |16762-817-16763-818-819-820-875-919-920 | 920|Aplidium        |pallidum        |       |      |
|                           |Aplidium nordmanni         |            |16762-817-16763-818-819-820-875-919-921 | 921|Aplidium        |nordmanni       |       |      |
|                           |Aplidium proliferum        |            |16762-817-16763-818-819-820-875-919-922 | 922|Aplidium        |proliferum      |       |      |
|                           |Aplidium punctum           |            |16762-817-16763-818-819-820-875-919-923 | 923|Aplidium        |punctum         |       |      |
|(Verrill, 1871)            |Aplidium glabrum           |            |16762-817-16763-818-819-820-875-919-924 | 924|Aplidium        |glabrum         |       |      |
|(Giard, 1872)              |Aplidium densum            |            |16762-817-16763-818-819-820-875-919-925 | 925|Aplidium        |densum          |       |      |
|(Herdman, 1886)            |Aplidium effrenatum        |            |16762-817-16763-818-819-820-875-919-926 | 926|Aplidium        |effrenatum      |       |      |
|Giard, 1872                |Didemnidae                 |            |16762-817-16763-818-819-820-927         | 927|Didemnidae      |                |       |      |
|Savigny, 1816              |Didemnum                   |            |16762-817-16763-818-819-820-927-928     | 928|Didemnum        |                |       |      |
|(Verrill, 1871)            |Didemnum albidum           |            |16762-817-16763-818-819-820-927-928-929 | 929|Didemnum        |albidum         |       |      |
|Ritter and Forsyth, 1917   |Didemnum carnulentum       |            |16762-817-16763-818-819-820-927-928-932 | 932|Didemnum        |carnulentum     |       |      |
|Savigny, 1816              |Didemnum candidum          |            |16762-817-16763-818-819-820-927-928-933 | 933|Didemnum        |candidum        |       |      |
|                           |Didemnum helgolandicum     |            |16762-817-16763-818-819-820-927-928-937 | 937|Didemnum        |helgolandicum   |       |      |
|                           |Didemnum gelatinosum       |            |16762-817-16763-818-819-820-927-928-938 | 938|Didemnum        |gelatinosum     |       |      |
|Van Name, 1924             |Didemnum vanderhorsti      |            |16762-817-16763-818-819-820-927-928-939 | 939|Didemnum        |vanderhorsti    |       |      |
|Hartmeyer, 1911            |Didemnum studeri           |            |16762-817-16763-818-819-820-927-928-940 | 940|Didemnum        |studeri         |       |      |
|(Herdman, 1886)            |Didemnum tenue             |            |16762-817-16763-818-819-820-927-928-941 | 941|Didemnum        |tenue           |       |      |
|(Sluiter, 1906)            |Didemnum biglans           |            |16762-817-16763-818-819-820-927-928-942 | 942|Didemnum        |biglans         |       |      |
|Arnbaeck, 1929             |Didemnum chilense          |            |16762-817-16763-818-819-820-927-928-943 | 943|Didemnum        |chilense        |       |      |
|Van Name, 1945             |Didemnum santaelenae       |            |16762-817-16763-818-819-820-927-928-944 | 944|Didemnum        |santaelenae     |       |      |
|(Van Name, 1902)           |Didemnum amethysteum       |            |16762-817-16763-818-819-820-927-928-945 | 945|Didemnum        |amethysteum     |       |      |
|Della Valle, 1881          |Trididemnum                |            |16762-817-16763-818-819-820-927-946     | 946|Trididemnum     |                |       |      |
|(Verrill, 1871)            |Trididemnum tenerum        |            |16762-817-16763-818-819-820-927-946-947 | 947|Trididemnum     |tenerum         |       |      |
```