# MagicItemTarotJava
/*
         Gabriel Maddock - 10 April, 2018
   
            ---Magic Item Generator---
      I haven't balanced these items at all. This is
   mainly a resource for me to use in my own campaigns.
   While some effects may seem unclear, the purpose
   of this code is to give players a new and exciting
   way to find magic items. It is pretty much up to the
   DM to fill in the gaps and incorporate the items into
   your own campaign. I created this generator with my
   very homebrewed campaign in mind.
   
      This generator either randomly picks tarot cards via
   a random number generator, or it can be used with a
   physical tarot deck. 
   
            V 1.3
*/

import java.util.Random;
import java.util.Scanner;

public class MagicItemTarot {
   public static void main(String args[]) {
     
      // Declare Variables
      int type = 0;
      int arcana = 0;
      int card = 0;
      int num = 0;
      
      Random ranNum = new Random();
      Scanner reader = new Scanner(System.in);
      
      char input = 'a';
      
      String itemType = "Tome";
      String other = "Void";  
      String suite = "heart";   
      
      // Ask for manual or random
      System.out.print("Manual input? (y/n) ");
      input = reader.next().charAt(0);
      
      // If manual, start setting variables
      if (input == 'y') {
         
         // Ask for card number
         System.out.print("Your card number: ");
         card = reader.nextInt();
         
         // Ask for suite
         System.out.print("Your card suite: ");
         suite = reader.next();
         suite = suite.toLowerCase();
         
         // Switch-case for each suite
         switch (suite) {
            case "hearts":
               type = 4;
               break;
            case "spades":
               type = 3;
               break;
            case "diamonds":
               type = 2;
               break;
            case "clubs":
               type = 1;
               break;    
            default:
               System.out.println("Enter hearts, spades, diamonds or clubs.");
            return;      
         }
         
         // Ask for Arcana number
         System.out.print("Your Arcana number (99 for arcana): ");
         arcana = reader.nextInt();
         
         while (arcana == 99) {
            System.out.println("0 - The Fool");
            System.out.println("1 - The Magician");
            System.out.println("2 - The High Priestess");
            System.out.println("3 - The Empress");
            System.out.println("4 - The Emperor");
            System.out.println("5 - The Hierophant");
            System.out.println("6 - The Lovers");
            System.out.println("7 - The Chariot");
            System.out.println("8 - Strength");
            System.out.println("9 - The Hermit");
            System.out.println("10 - Wheel of Fortune");
            System.out.println("11 - Justice");
            System.out.println("12 - The Hanged Man");
            System.out.println("13 - Death");
            System.out.println("14 - Temperance");
            System.out.println("15 - The Devil");
            System.out.println("16 - The Tower");
            System.out.println("17 - The Star");
            System.out.println("18 - The Moon");
            System.out.println("19 - The Sun");
            System.out.println("20 - Judgement");
            System.out.println("21 - The World");
            System.out.println(" ------------- ");
            
            // Ask for Arcana number
            System.out.print("Your Arcana number (? for arcana): ");
            arcana = reader.nextInt();
            }
         System.out.println(" ------------- ");
         
      } else if (input == 'n'){
      // Randomly generate three ints
      type = ranNum.nextInt(4) + 1;
      card = ranNum.nextInt(13)+1;
      arcana = ranNum.nextInt(22);
      } else {
         System.out.println("Enter y or n");
         return;
      }
      
      // Print suite
      System.out.print("Your suite is");
      
      if (type == 4) {
         System.out.println(" - hearts");
      } else if (type == 3) {
         System.out.println(" - spades");
      } else if (type == 2) {
         System.out.println(" - diamonds");
      } else {
         System.out.println(" - clubs");
      }
      
      // Print card num
      System.out.println("Your card is - " + card);
      
      // Print arcana
      System.out.print("Your arcana is");
      switch (arcana) {
               case 1:
                  System.out.println(" - The Magician");
                  break;
               case 2:
                  System.out.println(" - The High Priestess");
                  break;
               case 3:
                  System.out.println(" - The Empress");
                  break;
               case 4:
                  System.out.println(" - The Emperor");
                  break;
               case 5:
                  System.out.println(" - The Hierophant");
                  break;
               case 6:
                  System.out.println(" - The Lovers");
                  break;
               case 7:
                  System.out.println(" - The Chariot");
                  break;
               case 8:
                  System.out.println(" - Strength");
                  break;
               case 9:
                  System.out.println(" - The Hermit");
                  break;
               case 10:
                  System.out.println(" - Wheel of Fortune");
                  break;
               case 11:
                  System.out.println(" - Justice");
                  break;
               case 12:
                  System.out.println(" - The Hanged Man");
                  break;
               case 13:
                  System.out.println(" - Death");
                  break;
               case 14:
                  System.out.println(" - Temperence");
                  break;
               case 15:
                  System.out.println(" - The Devil");
                  break;
               case 16:
                  System.out.println(" - The Tower");
                  break;
               case 17:
                  System.out.println(" - The Star");
                  break;
               case 18:
                  System.out.println(" - The Moon");
                  break;
               case 19:
                  System.out.println(" - The Sun");
                  break;
               case 20:
                  System.out.println(" - Judgement");
                  break;
               case 21:
                  System.out.println(" - The World");
                  break;
               case 0:
                  System.out.println(" - The Fool");
                  break;
               default:
                  System.out.println("Enter an Arcana number.");
                  return;
            }
            
      System.out.println(" ------------- ");      
            
            if (type == 4) {
         System.out.print("A piece of armor ");
         switch (card) {
            case 1:
               itemType = "Helmet";
               break;
            case 2:
               itemType = "Leather";
               break;
            case 3:
               itemType = "Studded Leather";
               break;
            case 4:
               itemType = "Hide";
               break;
            case 5:
               itemType = "Scale Mail";
               break;
            case 6:
               itemType = "Breastplate";
               break;
            case 7:
               itemType = "Chain Mail";
               break;
            case 8:
               itemType = "Robe";
               break;
            case 9:
               itemType = "Boots";
               break;
            case 10:
               itemType = "Shield";
               break;
            case 11:
               itemType = "Hood";
               break;
            case 12:
               itemType = "Gauntlet";
               break;
            case 13:
               itemType = "Plate Mail";
               break;   
         }
         
      } else if (type == 3) {
         System.out.print("A ranged weapon ");
         switch (card) {
            case 1:
               itemType = "Shortbow";
               break;
            case 2:
               itemType = "Longbow";
               break;
            case 3:
               itemType = "Heavy Crossbow";
               break;
            case 4:
               itemType = "Sling";
               break;
            case 5:
               itemType = "Blowgun";
               break;
            case 6:
               itemType = "Net";
               break;
            case 7:
               itemType = "Spear";
               break;
            case 8:
               itemType = "Whip";
               break;
            case 9:
               itemType = "Grappling Hook";
               break;
            case 10:
               itemType = "Light Crossbow";
               break;
            case 11:
               itemType = "Stave";
               break;
            case 12:
               itemType = "Wand";
               break;
            case 13:
               itemType = "Arrow";
               break;   
         }
      } else if (type == 2) {
         System.out.print("A piece of jewelry ");
         switch (card) {
            case 1:
               itemType = "Crown";
               break;
            case 2:
               itemType = "Necklace";
               break;
            case 3:
               itemType = "Bracelet";
               break;
            case 4:
               itemType = "Ring";
               break;
            case 5:
               itemType = "Gem";
               break;
            case 6:
               itemType = "Box";
               break;
            case 7:
               itemType = "Earring";
               break;
            case 8:
               itemType = "Amulet";
               break;
            case 9:
               itemType = "Locket";
               break;
            case 10:
               itemType = "Armlet";
               break;
            case 11:
               itemType = "Lute";
               break;
            case 12:
               itemType = "Crystal Ball";
               break;
            case 13:
               itemType = "Coin";
               break;
         }
      } else {
         System.out.print("A melee weapon ");
         switch (card) {
            case 1:
               itemType = "Shortsword";
               break;
            case 2:
               itemType = "Longsword";
               break;
            case 3:
               itemType = "Club";
               break;
            case 4:
               itemType = "Dagger";
               break;
            case 5:
               itemType = "Hammer";
               break;
            case 6:
               itemType = "Greatsword";
               break;
            case 7:
               itemType = "Scimitar";
               break;
            case 8:
               itemType = "Quarterstaff";
               break;
            case 9:
               itemType = "Sickle";
               break;
            case 10:
               itemType = "Trident";
               break;
            case 11:
               itemType = "Hand Axe";
               break;
            case 12:
               itemType = "Greataxe";
               break;
            case 13:
               itemType = "Claw";
               break;
         }
      }

            switch (arcana) {
               case 1:
                  System.out.println("with ties to the four elements.");
                  num = ranNum.nextInt(4) + 1;
                  switch (num) {
                     case 1:
                        other = "Earth";
                        break;
                     case 2:
                        other = "Fire";
                        break;
                     case 3:
                        other = "Air";
                        break;
                     case 4:
                        other = "Water";
                        break;
                  }
                  System.out.println("This " + itemType + " is embued with " + other + ".");
                  // Weapon  - Deal force, fire, slashing, or ice damage
                  // Armor   - Resist force, fire, slashing, or ice damage
                  // Jewelry - other effects (it's a surprise ;) )
                  break;
               case 2:
                  System.out.println("with ties to higher powers.");
                  num = ranNum.nextInt(4) + 1;
                  switch (num) {
                     case 1:
                        other = "a god";
                        break;
                     case 2:
                        other = "a demon";
                        break;
                     case 3:
                        other = "an aberration";
                        break;
                     case 4:
                        other = "the fey";
                        break;
                     }
                  System.out.println("This " + itemType + " calls out to " + other + ".");
                  // The effect depends highly on which higher power ;)
                  break;
               case 3:
                  System.out.println("with ties to the natural world.");
                  System.out.println("This " + itemType + " increases plant growth.");
                  // Weapon  - Vines grow and grapple enemies when struck
                  // Armor   - Current terrain is counted as favored terrain
                  break;
               case 4:
                  System.out.println("with ties to domination.");
                  System.out.println("This " + itemType + " enhances authority.");
                  // Can cast compulsion
                  break;
               case 5:
                  System.out.println("with ties to creation.");
                  System.out.println("This " + itemType + " is highly desired.");
                  // Weapon  - Radiant damage
                  // Armor   - Resist necrotic
                  // Jewelry - Cast Turn Dead
                  // Everyone seems to really want your item
                  break;
               case 6:
                  System.out.println("with ties to the heart.");
                  System.out.println("This " + itemType + " shows its value in unions");
                  // Healing spells heal double
                  // Can cast charm person
                  break;
               case 7:
                  System.out.println("with ties to will power.");
                  System.out.println("This " + itemType + " reacts to aggression.");
                  // Advantage on attack rolls/saving throws in hostility
                  break;
               case 8:
                  System.out.println("with ties to physical strength.");
                  // Your next damage roll acts as full damage.
                  // You take damage based on how far your roll was from it.
                  // (you roll a 2 on a d8 and you deal 8 but take 6/2 damage)
                  break;
               case 9:
                  System.out.println("with ties to the soul.");
                  System.out.println("This " + itemType + " has an effect in isolation.");
                  // Bonus for saves against enchantment/persuasion/fear
                  // The item does something special when alone ;)
                  break;
               case 10:
                  System.out.println("with ties to luck itself.");
                  // ;)
                  break;
               case 11:
                  System.out.println("with ties to justice.");
                  System.out.println("This " + itemType + " reacts to cause and effect");
                  // 
                  break;
               case 12:
                  System.out.println("with ties to sacrifice.");
                  System.out.println("This " + itemType + " has benefits with self-harm.");
                  // When the user is damaged, the item gets charged with 1/2 the damage
                  // This damage can be expelled.
                  // Four charges, damage is lost with a rest
                  break;
               case 13:
                  System.out.println("with ties to transition.");
                  System.out.println("This " + itemType + " hungers for souls");
                  // Every intelligent creature slain with this blade has its soul absorbed by the item
                  // Every three souls gathered, the weapon gains a +1 necrotic bonus, capped at 3
                  // Souls return every long rest
                  break;
               case 14:
                  System.out.println("with ties to transformation.");
                  System.out.println("This " + itemType + " abides by equivalent exchange.");
                  // May be able to transform into an item of equal nature
                  break;
               case 15:
                  System.out.println("with ties to addiction.");
                  System.out.println("You may have a certain... attachment to this " + itemType + ".");
                  // The more you use this weapon, the stronger it gets.
                  // The devil attached gets stronger as well.
                  // 1 - The item glimmers with a golden material. + 1d4
                  // 2 - The gold of the item becomes accentuated with a deep red metal. + 1d6 Necrotic
                  // 3 - The red metal engulfs the item, black spikes emerge. + 2d6 Necrotic
                  // 4 - Yo Gabe you gotta come up with something for this.6
                  break;
               case 16:
                  System.out.println("with ties to disaster.");
                  System.out.println("Something feels off about this " + itemType + ".");
                  // Good luck... 
                  break;
               case 17:
                  System.out.println("with ties to hope.");
                  System.out.println("This " + itemType + " may help you find what you desire.");
                  // Ask the item a question and hold it to the skies. 
                  // Melee weapon casts a shadow leading towards the destination
                  // Ranged weapon ammo casts a shadow when on the ground
                  // Armor glows when near items/target/destination
                  break;
               case 18:
                  System.out.println("with ties to illusion.");
                  num = ranNum.nextInt(4) + 1;
                  switch (num) {
                     case 1:
                        other = "has an ominous aura.";
                        // fear
                        break;
                     case 2:
                        other = "seems to draw the sound from the room.";
                        // silence
                        break;
                     case 3:
                        other = "seems almost... opaque?";
                        // invisibility
                        break;
                     case 4:
                        other = "has a blurry form.";
                        // blur
                        break;
                     }
                  System.out.println("This " + itemType + other);
                  break;
               case 19:
                  System.out.println("with ties to warmth.");
                  num = ranNum.nextInt(4) + 1;
                  switch (num) {
                     case 1:
                        other = "positivity";
                        break;
                     case 2:
                        other = "anger";
                        break;
                     case 3:
                        other = "determination";
                        break;
                     case 4:
                        other = "fear";
                        break;
                     }
                  System.out.println("This " + itemType + " reacts to " + other + ".");
                  // Deal/resist fire damage
                  break;
               case 20:
                  System.out.println("with ties to judgement.");
                  System.out.println("This " + itemType + " may grant insight.");
                  // Advantage on insight
                  // Can cast judgement effect on enemies (weapons on hit)
                  //   Enemies have disadvantage on spell saving throws
                  break;
               case 21:
                  System.out.println("with ties to completion.");
                  num = ranNum.nextInt(4) + 1;
                  switch (num) {
                     case 1:
                        other = "completing a task";
                        break;
                     case 2:
                        other = "dealing the finishing blow";
                        break;
                     case 3:
                        other = "opening a chest";
                        break;
                     case 4:
                        other = "finishing a long rest";
                        break;
                     }
                  System.out.println("This " + itemType + " grants temporary hit points when " + other + ".");
                  // Grants temporary hit points
                  // Grants inspiration
                  break;
               case 0:
                  System.out.println("with ties to risk taking.");
                  System.out.println("This " + itemType + " grants advantage in spontaneity.");
                  // Grants advantage when characters take risky actions
                  break;
            }

   }
}
