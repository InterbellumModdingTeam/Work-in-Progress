########################################################################################################
## This is the OOB file example, with ## marks the values that need changing are highlighted          ##
## Cheer [NL]ibahalii
########################################################################################################

##Creating a new division template, need to make a new one for each division template you want.
division_template = {
	name = "" ##How will this thing be named?

	division_names_group = CHI_INF_1 ## Do not change, unless you have your own name file for the units.
	##Which regiment sits where X = Down and UP, Y being left and right positions in the template.
	regiments = {
		infantry = { x = 0 y = 0 }
		cavalry = { x = 1 y = 0 }
		light_armor = { x = 2 y = 0}
	}
	##IF this unit has a support brigade where and what is it? only X is needed.
	support = {
		recon = { x = 0 y = 0 }      # Motorized recon inf bn
	}
	## How important is this unit? 0 = Reserves, 1 = Normal, 2 = Elite
	## Deciding factor in equipment alocation. (0 = red stripes(last), 1 = no stripes(normal), 2 = Orange strips(prio))
	##Here the unit in the example is a 'Elite' unit, and will recieve its equipment before others of a lower priority.
	priority = 2
}

##The name of the division on a map(if there is one deployed already..
units = {
	##create more armies(divisions) using the 'division = { } tag
	division = {
		name = "" ## What name will this unit get?
		location = ## what PROVINCE is this unit standing?(NOTE this CANNOT be a state_ID, it has to be a province_ID).
		division_template = "" ##What template does this unit use?(has to be a name from one of the templates you created above.
		start_experience_factor = 0 ##How much XP does this unit have?\
		start_equipment_factor = 0 ##How much % of their equipment does the unit have? 0 = 0%. 1 = 100% use decimals to set a value inbetween, per example 0.65 = 65% of their total needed equipment
	}

##What factories of the country are in use for what.
### Starting Equipment ###
instant_effect = {
	add_equipment_production = {
		equipment = {
			type = infantry_equipment_0 ##type of equipment = rifles
			creator = "CHI" ##Which nation designed this piece of equipment(other country would make it license production)
		}
		requested_factories = 0 ##How many Factories are working on this.
		progress = 0 ## How far are they with 1 piece of equipment(more important for tanks/ships etc).
		efficiency = 0 ## How effective(of the country MAX efficiency is this line running)
		
	}
}
##To add more, just add more of the coding from above, and change the equipment type, you can que up anything, as long as the country has the factories/docks for it and the tech unlocked for it.