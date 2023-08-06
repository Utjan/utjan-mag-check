# utjan-mag-check
Allows animators to make mag check animations

My previous implementation of this was an edit of the Ammo Check script, but mag check is now it's own script which avoids load order or conflict issues.
Still requires Ammo Check from Mags Redux or Standalone.

Now uses Aoldri's Common Animations to automate mag check variations (jams, empty mag, aiming)

Uses Unlocalizer feature of Modded Exes to access ammo check script data. The script will fall back to a less flexible workaround if it can't use Unlocalizer.

Does not work if an animation mod has installed the old mag check script. An error will show in the console if it's detected.

## How to use
Here is an example of mag check animations added to the hud section of your weapon:

```
anm_ammo_check                           = barry_magcheck_svu_hands, barry_magcheck_svu
anm_ammo_check_empty                     = barry_magcheck_svu_hands, barry_magcheck_svu_empty
anm_ammo_check_no_mag                    = barry_magcheck_svu_nomag_hands, barry_magcheck_svu_nomag
anm_ammo_check_jammed                    = barry_magcheck_svu_hands, barry_magcheck_svu_jammed
anm_ammo_check_empty_jammed              = barry_magcheck_svu_hands, barry_magcheck_svu_empty_jammed
anm_ammo_check_aim                       = barry_magcheck_svu_hands_ads, barry_magcheck_svu_ads
anm_ammo_check_empty_aim                 = barry_magcheck_svu_hands_ads, barry_magcheck_svu_empty_ads
anm_ammo_check_aim_jammed                = barry_magcheck_svu_hands_ads, barry_magcheck_svu_jammed_ads
anm_ammo_check_empty_aim_jammed          = barry_magcheck_svu_hands_ads, barry_magcheck_svu_jammed_ads
```

Here is an example of adding sounds to the mag checks in the sounds section

```
scripted_snd_ammo_check                  = weapons\svu\barry_magcheck
scripted_snd_ammo_check_empty_aim_jammed = weapons\svu\barry_magcheck
scripted_snd_ammo_check_jammed           = weapons\svu\barry_magcheck
scripted_snd_ammo_check_empty_jammed     = weapons\svu\barry_magcheck
scripted_snd_ammo_check_aim              = weapons\svu\barry_magcheck
scripted_snd_ammo_check_empty_aim        = weapons\svu\barry_magcheck
scripted_snd_ammo_check_aim_jammed       = weapons\svu\barry_magcheck
scripted_snd_ammo_check_empty            = weapons\svu\barry_magcheck
scripted_snd_ammo_check_no_mag           = weapons\svu\barry_magcheck_nomag
```
