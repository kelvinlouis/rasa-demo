## new to rasa + not new to chatbots + not migrating
* greet
    - utter_greet
    - utter_inform_privacypolicy
    - utter_ask_goal
* how_to_get_started
    - utter_getstarted
    - utter_first_bot_with_rasa
* mood_confirm
    - action_set_onboarding
    - slot{"onboarding": true}
    - utter_built_bot_before
* mood_confirm
    - utter_ask_migration
* deny
    - utter_explain_stack
    - utter_stack_details
    - utter_explain_nlucore
* mood_confirm OR how_to_get_started{"product":"stack"}
    - utter_explain_nlu
    - utter_explain_core
    - utter_tryout
* how_to_get_started{"product":"core"} OR mood_confirm OR how_to_get_started{"product":"stack"}
    - utter_quickstart
    - utter_anything_else

## new to rasa + not new to chatbots + migrating from dialogflow
* greet
    - utter_greet
    - utter_inform_privacypolicy
    - utter_ask_goal
* how_to_get_started
    - utter_getstarted
    - utter_first_bot_with_rasa
* mood_confirm
    - action_set_onboarding
    - slot{"onboarding": true}
    - utter_built_bot_before
* mood_confirm
    - utter_ask_migration
* switch{"current_api": "dialogflow"}
    - utter_switch_dialogflow
    - utter_anything_else

## new to rasa + not new to chatbots + migrating from luis
* greet
    - utter_greet
    - utter_inform_privacypolicy
    - utter_ask_goal
* how_to_get_started
    - utter_getstarted
    - utter_first_bot_with_rasa
* mood_confirm
    - action_set_onboarding
    - slot{"onboarding": true}
    - utter_built_bot_before
* mood_confirm
    - utter_ask_migration
* switch{"current_api": "luis"}
    - utter_switch_luis
    - utter_anything_else

## new to rasa + not new to chatbots + migrating from something else
* greet
    - utter_greet
    - utter_inform_privacypolicy
    - utter_ask_goal
* how_to_get_started
    - utter_getstarted
    - utter_first_bot_with_rasa
* mood_confirm
    - action_set_onboarding
    - slot{"onboarding": true}
    - utter_built_bot_before
* mood_confirm
    - utter_ask_migration
* switch
    - action_store_unknown_product
    - utter_no_guide_for_switch
    - utter_anything_else

##  migrating from dialogflow
* greet
    - utter_greet
    - utter_inform_privacypolicy
    - utter_ask_goal
* how_to_get_started
    - utter_getstarted
    - utter_first_bot_with_rasa
* mood_confirm
    - action_set_onboarding
    - slot{"onboarding": true}
    - utter_built_bot_before
* mood_confirm
    - utter_ask_migration
* mood_confirm
    - utter_ask_which_tool
* switch{"current_api": "dialogflow"}
    - utter_switch_dialogflow
    - utter_anything_else

## new to rasa + not new to chatbots + migrating from luis
* greet
    - utter_greet
    - utter_inform_privacypolicy
    - utter_ask_goal
* how_to_get_started
    - utter_getstarted
    - utter_first_bot_with_rasa
* mood_confirm
    - action_set_onboarding
    - slot{"onboarding": true}
    - utter_built_bot_before
* mood_confirm
    - utter_ask_migration
* mood_confirm
    - utter_ask_which_tool
* switch{"current_api": "luis"}
    - utter_switch_luis
    - utter_anything_else

## new to rasa + not new to chatbots + migrating from something else
* greet
    - utter_greet
    - utter_inform_privacypolicy
    - utter_ask_goal
* how_to_get_started
    - utter_getstarted
    - utter_first_bot_with_rasa
* mood_confirm
    - action_set_onboarding
    - slot{"onboarding": true}
    - utter_built_bot_before
* mood_confirm
    - utter_ask_migration
* mood_confirm
    - utter_ask_which_tool
* switch
    - action_store_unknown_product
    - utter_no_guide_for_switch
    - utter_anything_else


## new to rasa/bots, explain stack and try it out
* greet
    - utter_greet
    - utter_inform_privacypolicy
    - utter_ask_goal
* how_to_get_started
    - utter_getstarted
    - utter_first_bot_with_rasa
* mood_confirm
    - action_set_onboarding
    - slot{"onboarding": true}
    - utter_built_bot_before
* deny
    - utter_explain_stack
    - utter_stack_details
    - utter_explain_nlucore
* mood_confirm OR how_to_get_started{"product":"stack"}
    - utter_explain_nlu
    - utter_explain_core
    - utter_tryout
* how_to_get_started{"product":"core"} OR mood_confirm OR how_to_get_started{"product":"stack"}
    - utter_quickstart
    - utter_anything_else

## new to rasa/bots, explain core and try out stack
* greet
    - utter_greet
    - utter_inform_privacypolicy
    - utter_ask_goal
* how_to_get_started
    - utter_getstarted
    - utter_first_bot_with_rasa
* mood_confirm
    - action_set_onboarding
    - slot{"onboarding": true}
    - utter_built_bot_before
* deny
    - utter_explain_stack
    - utter_stack_details
    - utter_explain_nlucore
* how_to_get_started{"product": "core"}
    - utter_explain_core
    - utter_also_explain_nlu
* deny
    - utter_tryout
* how_to_get_started{"product":"core"} OR mood_confirm OR how_to_get_started{"product":"stack"}
    - utter_quickstart
    - utter_anything_else

## new to rasa/bots, explain core, then nlu and try out stack
* greet
    - utter_greet
    - utter_inform_privacypolicy
    - utter_ask_goal
* how_to_get_started
    - utter_getstarted
    - utter_first_bot_with_rasa
* mood_confirm
    - action_set_onboarding
    - slot{"onboarding": true}
    - utter_built_bot_before
* deny
    - utter_explain_stack
    - utter_stack_details
    - utter_explain_nlucore
* how_to_get_started{"product": "core"}
    - utter_explain_core
    - utter_also_explain_nlu
* mood_confirm
    - utter_explain_nlu
    - utter_tryout
* how_to_get_started{"product":"core"} OR mood_confirm OR how_to_get_started{"product":"stack"}
    - utter_quickstart
    - utter_anything_else

## new to rasa/bots, explain nlu and try out stack
* greet
    - utter_greet
    - utter_inform_privacypolicy
    - utter_ask_goal
* how_to_get_started
    - utter_getstarted
    - utter_first_bot_with_rasa
* mood_confirm
    - action_set_onboarding
    - slot{"onboarding": true}
    - utter_built_bot_before
* deny
    - utter_explain_stack
    - utter_stack_details
    - utter_explain_nlucore
* how_to_get_started{"product": "nlu"}
    - utter_explain_nlu
    - utter_also_explain_core
* deny
    - utter_tryout
* how_to_get_started{"product":"core"} OR mood_confirm OR how_to_get_started{"product":"stack"}
    - utter_quickstart
    - utter_anything_else

## new to rasa/bots, explain nlu then core and try out stack
* greet
    - utter_greet
    - utter_inform_privacypolicy
    - utter_ask_goal
* how_to_get_started
    - utter_getstarted
    - utter_first_bot_with_rasa
* mood_confirm
    - action_set_onboarding
    - slot{"onboarding": true}
    - utter_built_bot_before
* deny
    - utter_explain_stack
    - utter_stack_details
    - utter_explain_nlucore
* how_to_get_started{"product": "nlu"}
    - utter_explain_nlu
    - utter_also_explain_core
* mood_confirm
    - utter_explain_core
    - utter_tryout
* how_to_get_started{"product":"core"} OR mood_confirm OR how_to_get_started{"product":"stack"}
    - utter_quickstart
    - utter_anything_else


## new to rasa/bots, don't explain and try out stack
* greet
    - utter_greet
    - utter_inform_privacypolicy
    - utter_ask_goal
* how_to_get_started
    - utter_getstarted
    - utter_first_bot_with_rasa
* mood_confirm
    - action_set_onboarding
    - slot{"onboarding": true}
    - utter_built_bot_before
* deny
    - utter_explain_stack
    - utter_stack_details
    - utter_explain_nlucore
* deny
    - utter_tryout
* how_to_get_started{"product":"core"} OR mood_confirm OR how_to_get_started{"product":"stack"}
    - utter_quickstart
    - utter_anything_else


## new to rasa/bots, explain and skip to installation
* greet
    - utter_greet
    - utter_inform_privacypolicy
    - utter_ask_goal
* how_to_get_started
    - utter_getstarted
    - utter_first_bot_with_rasa
* mood_confirm
    - action_set_onboarding
    - slot{"onboarding": true}
    - utter_built_bot_before
* deny
    - utter_explain_stack
    - utter_stack_details
    - utter_explain_nlucore
* mood_confirm OR how_to_get_started{"product":"stack"}
    - utter_explain_nlu
    - utter_explain_core
    - utter_tryout
* deny
    - utter_direct_install
    - utter_anything_else

## new to rasa/bots, explain nlu and skip to installation
* greet
    - utter_greet
    - utter_inform_privacypolicy
    - utter_ask_goal
* how_to_get_started
    - utter_getstarted
    - utter_first_bot_with_rasa
* mood_confirm
    - action_set_onboarding
    - slot{"onboarding": true}
    - utter_built_bot_before
* deny
    - utter_explain_stack
    - utter_stack_details
    - utter_explain_nlucore
* how_to_get_started{"product": "nlu"}
    - utter_explain_nlu
    - utter_also_explain_core
* deny
    - utter_tryout
* deny
    - utter_direct_install
    - utter_anything_else

## new to rasa/bots, explain core and skip to installation
* greet
    - utter_greet
    - utter_inform_privacypolicy
    - utter_ask_goal
* how_to_get_started
    - utter_getstarted
    - utter_first_bot_with_rasa
* mood_confirm
    - action_set_onboarding
    - slot{"onboarding": true}
    - utter_built_bot_before
* deny
    - utter_explain_stack
    - utter_stack_details
    - utter_explain_nlucore
* how_to_get_started{"product": "core"}
    - utter_explain_core
    - utter_also_explain_nlu
* deny
    - utter_tryout
* deny
    - utter_direct_install
    - utter_anything_else

## new to rasa/bots, explain core and try nlu
* greet
    - utter_greet
    - utter_inform_privacypolicy
    - utter_ask_goal
* how_to_get_started
    - utter_getstarted
    - utter_first_bot_with_rasa
* mood_confirm
    - action_set_onboarding
    - slot{"onboarding": true}
    - utter_built_bot_before
* deny
    - utter_explain_stack
    - utter_stack_details
    - utter_explain_nlucore
* how_to_get_started{"product": "core"}
    - utter_explain_core
    - utter_also_explain_nlu
* deny
    - utter_tryout
* how_to_get_started{"product": "nlu"}
    - utter_quickstart_nlu_only
    - utter_anything_else

## new to rasa/bots, explain nlu and try nlu
* greet
    - utter_greet
    - utter_inform_privacypolicy
    - utter_ask_goal
* how_to_get_started
    - utter_getstarted
    - utter_first_bot_with_rasa
* mood_confirm
    - action_set_onboarding
    - slot{"onboarding": true}
    - utter_built_bot_before
* deny
    - utter_explain_stack
    - utter_stack_details
    - utter_explain_nlucore
* how_to_get_started{"product": "nlu"}
    - utter_explain_nlu
    - utter_also_explain_core
* deny
    - utter_tryout
* how_to_get_started{"product": "nlu"}
    - utter_quickstart_nlu_only
    - utter_anything_else

## new to rasa/bots, explain both and try nlu
* greet
    - utter_greet
    - utter_inform_privacypolicy
    - utter_ask_goal
* how_to_get_started
    - utter_getstarted
    - utter_first_bot_with_rasa
* mood_confirm
    - action_set_onboarding
    - slot{"onboarding": true}
    - utter_built_bot_before
* deny
    - utter_explain_stack
    - utter_stack_details
    - utter_explain_nlucore
* mood_confirm OR how_to_get_started{"product":"stack"}
    - utter_explain_nlu
    - utter_explain_core
    - utter_tryout
* how_to_get_started{"product": "nlu"}
    - utter_quickstart_nlu_only
    - utter_anything_else

## new to rasa/bots, explain nlu then core and try nlu
* greet
    - utter_greet
    - utter_inform_privacypolicy
    - utter_ask_goal
* how_to_get_started
    - utter_getstarted
    - utter_first_bot_with_rasa
* mood_confirm
    - action_set_onboarding
    - slot{"onboarding": true}
    - utter_built_bot_before
* deny
    - utter_explain_stack
    - utter_stack_details
    - utter_explain_nlucore
* how_to_get_started{"product": "nlu"}
    - utter_explain_nlu
    - utter_also_explain_core
* mood_confirm
    - utter_explain_core
    - utter_tryout
* how_to_get_started{"product": "nlu"}
    - utter_quickstart_nlu_only
    - utter_anything_else


## not new to rasa + not interested in products
* greet
    - utter_greet
    - utter_inform_privacypolicy
    - utter_ask_goal
* how_to_get_started
    - utter_getstarted
    - utter_first_bot_with_rasa
* deny
    - action_set_onboarding
    - slot{"onboarding": false}
    - utter_ask_which_product
* deny
    - utter_thumbsup

## not new to rasa + core
* greet
    - utter_greet
    - utter_inform_privacypolicy
    - utter_ask_goal
* how_to_get_started
    - utter_getstarted
    - utter_first_bot_with_rasa
* deny
    - action_set_onboarding
    - slot{"onboarding": false}
    - utter_ask_which_product
* how_to_get_started{"product": "core"}
    - utter_core_tutorial
    - utter_anything_else

## skip to info on core
* how_to_get_started{"product": "core"}
    - utter_core_tutorial
    - utter_anything_else

## skip to info on core
* greet
    - utter_greet
    - utter_inform_privacypolicy
    - utter_ask_goal
* how_to_get_started{"product": "core"}
    - utter_core_tutorial
    - utter_anything_else

## not new to rasa + nlu + nothing special
* greet
    - utter_greet
    - utter_inform_privacypolicy
    - utter_ask_goal
* how_to_get_started
    - utter_getstarted
    - utter_first_bot_with_rasa
* deny
    - action_set_onboarding
    - slot{"onboarding": false}
    - utter_ask_which_product
* how_to_get_started{"product": "nlu"}
    - utter_ask_for_nlu_specifics
* deny
    - utter_quickstart_nlu_only
    - utter_anything_else

## not new to rasa + nlu + unknown topic
* greet
    - utter_greet
    - utter_inform_privacypolicy
    - utter_ask_goal
* how_to_get_started
    - utter_getstarted
    - utter_first_bot_with_rasa
* deny
    - action_set_onboarding
    - slot{"onboarding": false}
    - utter_ask_which_product
* how_to_get_started{"product": "nlu"}
    - utter_ask_for_nlu_specifics
* nlu_info
    - action_store_unknown_nlu_part
    - utter_dont_know_nlu_part
    - utter_search_bar
    - utter_anything_else

## not new to rasa + nlu + intent + no recommendation
* greet
    - utter_greet
    - utter_inform_privacypolicy
    - utter_ask_goal
* how_to_get_started
    - utter_getstarted
    - utter_first_bot_with_rasa
* deny
    - action_set_onboarding
    - slot{"onboarding": false}
    - utter_ask_which_product
* how_to_get_started{"product": "nlu"}
    - utter_ask_for_nlu_specifics
* nlu_info{"nlu_part": "intent classification"}
    - utter_nlu_intent_tutorial
    - utter_offer_recommendation
* deny
    - utter_thumbsup
    - utter_anything_else

## not new to rasa + nlu + intent + pipeline recommendation, spacy
* greet
    - utter_greet
    - utter_inform_privacypolicy
    - utter_ask_goal
* how_to_get_started
    - utter_getstarted
    - utter_first_bot_with_rasa
* deny
    - action_set_onboarding
    - slot{"onboarding": false}
    - utter_ask_which_product
* how_to_get_started{"product": "nlu"}
    - utter_ask_for_nlu_specifics
* nlu_info{"nlu_part": "intent classification"}
    - utter_nlu_intent_tutorial
    - utter_offer_recommendation
* pipeline_recommendation OR mood_confirm
    - utter_what_language
* enter_data{"language": "en"}
    - action_store_bot_language
    - slot{"can_use_spacy": true}
    - utter_spacy_or_tensorflow
    - utter_anything_else

## not new to rasa + nlu + intent + pipeline recommendation, not spacy
* greet
    - utter_greet
    - utter_inform_privacypolicy
    - utter_ask_goal
* how_to_get_started
    - utter_getstarted
    - utter_first_bot_with_rasa
* deny
    - action_set_onboarding
    - slot{"onboarding": false}
    - utter_ask_which_product
* how_to_get_started{"product": "nlu"}
    - utter_ask_for_nlu_specifics
* nlu_info{"nlu_part": "intent classification"}
    - utter_nlu_intent_tutorial
    - utter_offer_recommendation
* pipeline_recommendation OR mood_confirm
    - utter_what_language
* enter_data{"language": "en"}
    - action_store_bot_language
    - slot{"can_use_spacy": false}
    - utter_tensorflow
    - utter_anything_else

## not new to rasa + nlu + intent + tool recommendation
* greet
    - utter_greet
    - utter_inform_privacypolicy
    - utter_ask_goal
* how_to_get_started
    - utter_getstarted
    - utter_first_bot_with_rasa
* deny
    - action_set_onboarding
    - slot{"onboarding": false}
    - utter_ask_which_product
* how_to_get_started{"product": "nlu"}
    - utter_ask_for_nlu_specifics
* nlu_info{"nlu_part": "intent classification"}
    - utter_nlu_intent_tutorial
    - utter_offer_recommendation
* nlu_generation_tool_recommendation
    - utter_nlu_tools

## not new to rasa + nlu + entity + no recommendation
* greet
    - utter_greet
    - utter_inform_privacypolicy
    - utter_ask_goal
* how_to_get_started
    - utter_getstarted
    - utter_first_bot_with_rasa
* deny
    - action_set_onboarding
    - slot{"onboarding": false}
    - utter_ask_which_product
* how_to_get_started{"product": "nlu"}
    - utter_ask_for_nlu_specifics
* nlu_info{"nlu_part": "entity recognition"}
    - utter_nlu_entity_tutorial
    - utter_offer_recommendation
* deny
    - utter_thumbsup
    - utter_anything_else

## not new to rasa + nlu + entity + pipeline spacy
* greet
    - utter_greet
    - utter_inform_privacypolicy
    - utter_ask_goal
* how_to_get_started
    - utter_getstarted
    - utter_first_bot_with_rasa
* deny
    - action_set_onboarding
    - slot{"onboarding": false}
    - utter_ask_which_product
* how_to_get_started{"product": "nlu"}
    - utter_ask_for_nlu_specifics
* nlu_info{"nlu_part": "entity recognition"}
    - utter_nlu_entity_tutorial
    - utter_offer_recommendation
* pipeline_recommendation OR mood_confirm
    - utter_ask_entities
* enter_data{"entity": "name"}
    - action_store_entity_extractor
    - slot{"entity_extractor": "ner_spacy"}
    - utter_spacy
    - utter_anything_else

## not new to rasa + nlu + entity + pipeline duckling
* greet
    - utter_greet
    - utter_inform_privacypolicy
    - utter_ask_goal
* how_to_get_started
    - utter_getstarted
    - utter_first_bot_with_rasa
* deny
    - action_set_onboarding
    - slot{"onboarding": false}
    - utter_ask_which_product
* how_to_get_started{"product": "nlu"}
    - utter_ask_for_nlu_specifics
* nlu_info{"nlu_part": "entity recognition"}
    - utter_nlu_entity_tutorial
    - utter_offer_recommendation
* pipeline_recommendation OR mood_confirm
    - utter_ask_entities
* enter_data{"entity": "date ranges"}
    - action_store_entity_extractor
    - slot{"entity_extractor": "ner_duckling_http"}
    - utter_duckling
    - utter_anything_else

## not new to rasa + nlu + entity + pipeline ner_crf
* greet
    - utter_greet
    - utter_inform_privacypolicy
    - utter_ask_goal
* how_to_get_started
    - utter_getstarted
    - utter_first_bot_with_rasa
* deny
    - action_set_onboarding
    - slot{"onboarding": false}
    - utter_ask_which_product
* how_to_get_started{"product": "nlu"}
    - utter_ask_for_nlu_specifics
* nlu_info{"nlu_part": "entity recognition"}
    - utter_nlu_entity_tutorial
    - utter_offer_recommendation
* pipeline_recommendation OR mood_confirm
    - utter_ask_entities
* enter_data{"entity": "some custom entity"}
    - action_store_entity_extractor
    - slot{"entity_extractor": "ner_crf"}
    - utter_crf
    - utter_anything_else

## not new to rasa + nlu + entity + duckling info
* greet
    - utter_greet
    - utter_inform_privacypolicy
    - utter_ask_goal
* how_to_get_started
    - utter_getstarted
    - utter_first_bot_with_rasa
* deny
    - action_set_onboarding
    - slot{"onboarding": false}
    - utter_ask_which_product
* how_to_get_started{"product": "nlu"}
    - utter_ask_for_nlu_specifics
* nlu_info{"nlu_part": "duckling"}
    - utter_duckling_info
    - utter_anything_else

## skip to info on nlu entities
* nlu_info{"nlu_part": "entity recognition"}
    - utter_nlu_entity_tutorial
    - utter_offer_recommendation

## skip to info on nlu intents
* nlu_info{"nlu_part": "intent classification"}
    - utter_nlu_intent_tutorial
    - utter_offer_recommendation

## skip to info on nlu intents
* nlu_info{"nlu_part": "duckling"}
    - utter_duckling_info
    - utter_anything_else

## switch immediately to luis
* switch{"current_api":"luis"}
    - utter_switch_luis
    - utter_anything_else

## switch immediately to dialogflow
* switch{"current_api": "dialogflow"}
    - utter_switch_dialogflow
    - utter_anything_else

## how much does rasa cost
* rasa_cost
    - utter_rasa_cost
    - utter_anything_else

## source code
* source_code
    - utter_source_code
    - utter_anything_else

## how to get started without privacy policy
* how_to_get_started
    - utter_getstarted
    - utter_first_bot_with_rasa
* mood_confirm
    - action_set_onboarding
    - slot{"onboarding": true}
    - utter_built_bot_before
* mood_confirm
    - utter_ask_migration
* deny
    - utter_explain_stack
    - utter_stack_details
    - utter_explain_nlucore
* mood_confirm OR how_to_get_started{"product":"stack"}
    - utter_explain_nlu
    - utter_explain_core
    - utter_tryout
* how_to_get_started{"product":"core"} OR mood_confirm OR how_to_get_started{"product":"stack"}
    - utter_quickstart
    - utter_anything_else
