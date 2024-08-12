classDiagram
direction BT
class addresses {
   varchar(255) address
   varchar(255) city
   varchar(500) description
   varchar(255) email
   double latitude
   double longitude
   varchar(255) open_hours
   varchar(255) phone
   bigint images_id
   bigint metro_id
   varchar(255) address_complex
   varchar(255) address_op
   varchar(255) phone_op
   varchar(255) phone_oz
   varchar(255) nav_link_complex
   varchar(255) nav_link_op
   bigint id
}
class admins {
   varchar(255) login
   varchar(255) password
   bigint id
}
class article2categories {
   bigint article_id
   varchar(255) category
}
class article2pins {
   bigint article_id
   bigint pin_id
}
class article2projects {
   bigint article_id
   varchar(255) project
}
class articles {
   varchar(255) header
   varchar(1000) mini_text
   varchar(1000) preview_text
   varchar(255) project_code
   bigint content_id
   bigint gallery_id
   bigint image_id
   bigint region_id
   varchar(255) positition
   varchar(255) position
   varchar(255) category
   varchar(255) article_type
   text html
   varchar(255) view_type
   varchar(1000) video_link
   varchar(255) header_color
   bigint id
}
class design_features {
   varchar(255) main_color
   varchar(255) secondary_color
   bigint loader_id
   varchar(255) color_actions
   varchar(255) color_calculator
   varchar(255) color_conditions
   varchar(255) color_features
   varchar(255) color_finishing
   varchar(255) color_flats
   varchar(255) color_gallery
   varchar(255) color_locations
   varchar(255) color_map
   varchar(255) color_plans
   varchar(255) color_progress
   bigint header_logo_id
   bigint map_logo_id
   bigint id
}
class galleries {
   varchar(1000) description
   varchar(255) file_type
   bigint owner_id
   bit(1) to_hide
   varchar(255) display_name
   int priority
   bigint parent_id
   varchar(255) display_name_accent_color
   bigint id
}
class gallery2images {
   bigint gallery_id
   bigint media_id
}
class gallery_block2galleries {
   bigint gallery_block_id
   bigint galleries_id
}
class gallery_blocks {
   varchar(1000) description
   bit(1) to_hide
   bigint id
}
class main_sliders {
   bigint region_id
   varchar(255) title
   bigint id
}
class map_selectors {
   text json_string
   varchar(255) project_code
}
class medias {
   varchar(255) description
   varchar(255) display_name
   varchar(255) file
   varchar(255) file_name
   varchar(255) file_type
   varchar(255) project_code
   int priority
   varchar(255) embed
   varchar(255) link
   varchar(255) link_name
   varchar(255) content_type
   varchar(255) mime_type
   varchar(255) original_file_name
   bigint file_size
   varchar(255) extension
   bigint id
}
class metro {
   varchar(255) color
   varchar(255) name
   varchar(255) type
   bigint region_id
   bigint id
}
class page_settings {
   varchar(31) dtype
   varchar(255) settings_key
   varchar(255) value
   bit(1) to_hide
   bit(1) show_finishing
   bit(1) show_gallery
   bit(1) show_mortgage_calculator
   bit(1) show_purchase_terms
   bigint id
}
class participants_blocks {
   bigint id
}
class pins {
   bit(1) available
   varchar(255) value
   bigint id
}
class project2buildings {
   bigint project_id
   bigint buildings_id
}
class project2queues {
   bigint project_id
   bigint queues_id
}
class project_building2sections {
   bigint building_id
   bigint project_section_floors_id
}
class project_buildings {
   varchar(1000) address
   bigint building_id
   int building_num
   varchar(255) building_state
   varchar(255) building_type
   int built_year
   int count_free
   int count_total
   varchar(255) delivery_period
   int floors_count
   bit(1) key_issuance
   varchar(255) mounting_beginning
   varchar(255) name
   int ready_quarter
   int section_count
   int status
   bigint queue_id
   bit(1) active
   varchar(255) real_building_num
   bigint id
}
class project_characteristics {
   varchar(255) description
   varchar(255) location
   varchar(255) parking
   varchar(255) project_class
   varchar(255) sale_status
   bit(1) live
   bit(1) sale_start
   varchar(255) time_by_metro
   varchar(255) time_to_metro
   varchar(255) mortgage_min_price
   varchar(255) min_price
   bigint id
}
class project_common_prices {
   bigint id
}
class project_data_by_rooms {
   double cost
   double count
   bigint room_count
   double square
   bigint id
}
class project_data_by_rooms2buildings {
   bigint building_id
   bigint by_rooms_id
}
class project_data_by_rooms2projects {
   bigint price_id
   bigint by_rooms_id
}
class project_documents_blocks {
   varchar(1000) description
   bigint documents_id
   bigint id
}
class project_extended_info {
   bigint about_id
   bigint benefits_id
   bigint contact_id
   bigint documents_id
   bigint features_id
   bigint finishing_id
   bigint gallery_id
   bigint general_plan_id
   bigint location_id
   bigint participants_id
   bigint progress_id
   bigint slider_id
   bigint plans_id
   bigint progress_data_id
   bigint documents_data_id
   bigint participants_block_id
   bigint id
}
class project_info {
   varchar(255) builder
   varchar(255) code
   bigint flats_number
   varchar(255) name
   varchar(255) site
   bigint address_id
   bigint characteristics_id
   bigint logo_image_id
   bigint main_image_id
   bigint prices_id
   bigint region_id
   bigint statuses_id
   varchar(255) sub_domen
   bit(1) to_show
   int priority
   bigint design_features_id
   bit(1) to_hide
   varchar(255) guid
   varchar(255) tour3d
   bigint presentation_id
   bigint id
}
class project_participant_block2participants {
   bigint block_id
   bigint participants_id
}
class project_participants {
   varchar(1000) description
   varchar(255) header
   int priority
   varchar(255) site
   bigint logo_id
   bigint id
}
class project_progress {
   varchar(1000) description
   bit(1) to_hide
   bigint id
}
class project_progress2progress_unit_blocks {
   bigint progress_id
   bigint progress_unit_blocks_id
}
class project_progress_blocks2progress_units {
   bigint progress_unit_block_id
   bigint progress_units_id
}
class project_progress_unit_blocks {
   varchar(255) grouped_by
   varchar(255) name
   int priority
   bit(1) to_hide
   bigint id
}
class project_progress_units {
   datetime(6) date
   bit(1) to_hide
   bigint gallery_block_id
   bigint id
}
class project_queues {
   varchar(255) building_state
   int built_year
   bit(1) key_issuance
   bigint number
   int ready_quarter
   bit(1) active
   bigint id
}
class project_section_floors {
   bigint floor_count
   bigint section
   bigint id
}
class project_statuses {
   bigint id
}
class publications {
   varchar(255) approval_status
   date date_created
   date display_date
   date last_modified_date
   varchar(255) link
   varchar(255) link_name
   bigint id
}
class regions {
   varchar(255) name
   varchar(255) code
   bigint id
}
class regions2codes {
   bigint region_id
   varchar(255) region
}
class settings_flat_page {
   bit(1) deleted
   bigint project_id
   bigint mortgage_calculator_settings_id
   bigint visibility_settings_id
   bigint block_position_settings_id
   bigint id
}
class settings_flat_page_block_positions {
   int features_position
   int finishing_position
   int mortgage_calculator_position
   int progress_position
   int purchase_terms_position
   int actions_position
   int benefits_position
   int flats_position
   int gallery_position
   int news_position
   bigint project_id
   int page_type
   bigint id
}
class settings_flat_page_block_visibility {
   bit(1) show_features
   bit(1) show_finishing
   bit(1) show_mortgage_calculator
   bit(1) show_purchase_terms
   bit(1) show_progress
   bigint id
}
class settings_mortgage_calculator {
   int cost
   int initial_payment
   int loan_period
   int max_cost
   int max_initial_payment
   int min_cost
   int min_initial_payment
   varchar(255) mortgage_type
   bigint project_id
   varchar(255) project_uuid
   bigint id
}
class settings_page_block_positions {
   int actions_position
   int benefits_position
   int features_position
   int finishing_position
   int flats_position
   int gallery_position
   int mortgage_calculator_position
   int news_position
   int page_type
   int progress_position
   bigint project_id
   int purchase_terms_position
   int location_position
   int window_view_position
   int participants_position
   bigint id
}
class statuses2projects {
   bigint status_id
   varchar(255) status
}
class tender_notices {
   datetime(6) created
   varchar(255) display_date
   datetime(6) last_updated
   varchar(1000) name
   bigint document_id
   bigint region_id
   bit(1) to_hide
   bigint id
}
class tenders {
   varchar(255) contract_month
   datetime(6) created
   datetime(6) last_updated
   varchar(255) name
   varchar(255) project
   int quarter
   varchar(255) region_name
   varchar(255) tender_type
   bit(1) to_hide
   int year
   bigint region_id
   bigint id
}
class users {
   varchar(255) user_role
   varchar(255) username
   bigint id
}
class visibility_settings {
   bit(1) show_finishing
   bit(1) show_gallery
   bit(1) show_mortgage_calculator
   bit(1) show_purchase_terms
   bigint id
}
class visual_selectors {
   text html
   varchar(255) project_code
   int selector_type
   int widget_type
   bigint id
}
class widgets {
   text html
   varchar(255) project_code
   int widget_type
   bigint id
}

addresses  -->  galleries : images_id:id
addresses  -->  metro : metro_id:id
admins  -->  users : id
article2categories  -->  articles : article_id:id
article2pins  -->  articles : article_id:id
article2pins  -->  pins : pin_id:id
article2projects  -->  articles : article_id:id
articles  -->  galleries : gallery_id:id
articles  -->  medias : image_id:id
articles  -->  medias : content_id:id
articles  -->  publications : id
articles  -->  regions : region_id:id
design_features  -->  medias : loader_id:id
design_features  -->  medias : header_logo_id:id
design_features  -->  medias : map_logo_id:id
gallery2images  -->  galleries : gallery_id:id
gallery2images  -->  medias : media_id:id
gallery_block2galleries  -->  galleries : galleries_id:id
gallery_block2galleries  -->  gallery_blocks : gallery_block_id:id
main_sliders  -->  galleries : id
main_sliders  -->  regions : region_id:id
metro  -->  regions : region_id:id
project2buildings  -->  project_buildings : buildings_id:id
project2buildings  -->  project_extended_info : project_id:id
project2queues  -->  project_info : project_id:id
project2queues  -->  project_queues : queues_id:id
project_building2sections  -->  project_buildings : building_id:id
project_building2sections  -->  project_section_floors : project_section_floors_id:id
project_buildings  -->  project_queues : queue_id:id
project_data_by_rooms2buildings  -->  project_buildings : building_id:id
project_data_by_rooms2buildings  -->  project_data_by_rooms : by_rooms_id:id
project_data_by_rooms2projects  -->  project_common_prices : price_id:id
project_data_by_rooms2projects  -->  project_data_by_rooms : by_rooms_id:id
project_documents_blocks  -->  galleries : documents_id:id
project_extended_info  -->  addresses : contact_id:id
project_extended_info  -->  galleries : slider_id:id
project_extended_info  -->  galleries : gallery_id:id
project_extended_info  -->  galleries : general_plan_id:id
project_extended_info  -->  galleries : about_id:id
project_extended_info  -->  galleries : benefits_id:id
project_extended_info  -->  gallery_blocks : finishing_id:id
project_extended_info  -->  gallery_blocks : documents_data_id:id
project_extended_info  -->  gallery_blocks : location_id:id
project_extended_info  -->  gallery_blocks : participants_block_id:id
project_extended_info  -->  gallery_blocks : features_id:id
project_extended_info  -->  gallery_blocks : gallery_id:id
project_extended_info  -->  gallery_blocks : progress_data_id:id
project_extended_info  -->  gallery_blocks : plans_id:id
project_extended_info  -->  participants_blocks : participants_id:id
project_extended_info  -->  participants_blocks : participants_block_id:id
project_extended_info  -->  project_documents_blocks : documents_id:id
project_extended_info  -->  project_info : id
project_extended_info  -->  project_progress : progress_id:id
project_info  -->  addresses : address_id:id
project_info  -->  design_features : design_features_id:id
project_info  -->  medias : presentation_id:id
project_info  -->  medias : main_image_id:id
project_info  -->  medias : logo_image_id:id
project_info  -->  project_characteristics : characteristics_id:id
project_info  -->  project_common_prices : prices_id:id
project_info  -->  project_statuses : statuses_id:id
project_info  -->  regions : region_id:id
project_participant_block2participants  -->  participants_blocks : block_id:id
project_participant_block2participants  -->  project_participants : participants_id:id
project_participants  -->  medias : logo_id:id
project_progress2progress_unit_blocks  -->  project_progress : progress_id:id
project_progress2progress_unit_blocks  -->  project_progress_unit_blocks : progress_unit_blocks_id:id
project_progress_blocks2progress_units  -->  project_progress_unit_blocks : progress_unit_block_id:id
project_progress_blocks2progress_units  -->  project_progress_units : progress_units_id:id
project_progress_units  -->  gallery_blocks : gallery_block_id:id
regions2codes  -->  regions : region_id:id
settings_flat_page  -->  settings_flat_page_block_positions : block_position_settings_id:id
settings_flat_page  -->  settings_flat_page_block_visibility : visibility_settings_id:id
settings_flat_page  -->  settings_mortgage_calculator : mortgage_calculator_settings_id:id
settings_flat_page  -->  visibility_settings : visibility_settings_id:id
settings_mortgage_calculator  -->  project_info : project_id:id
statuses2projects  -->  project_statuses : status_id:id
tender_notices  -->  medias : document_id:id
tender_notices  -->  regions : region_id:id
tenders  -->  regions : region_id:id
