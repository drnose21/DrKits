package drnose21.plugin;


import java.util.logging.Logger;


import org.bukkit.ChatColor;
import org.bukkit.Color;
import org.bukkit.Material;
import org.bukkit.command.Command;
import org.bukkit.command.CommandSender;
import org.bukkit.enchantments.Enchantment;
import org.bukkit.entity.Player;
import org.bukkit.event.Listener;

import org.bukkit.inventory.ItemStack;
import org.bukkit.inventory.PlayerInventory;
import org.bukkit.inventory.meta.ItemMeta;
import org.bukkit.inventory.meta.LeatherArmorMeta;
import org.bukkit.plugin.java.JavaPlugin;



public class drkits extends JavaPlugin implements Listener {
	public final Logger logger = Logger.getLogger("Minecraft");
	public static drkits plugin;
	
	
	public boolean onCommand(CommandSender sender, Command cmd, String commandLabel, String[] args)
	{
		ItemStack is = new ItemStack(Material.AIR);
		
		
		final Player player = (Player) sender;
		ItemStack helm = new ItemStack(Material.LEATHER_HELMET, 1);
		LeatherArmorMeta meta = (LeatherArmorMeta)helm.getItemMeta();
		meta.setColor(Color.RED);
		
		
		ItemStack chest = new ItemStack(Material.LEATHER_CHESTPLATE, 1);
		LeatherArmorMeta meta1 = (LeatherArmorMeta)chest.getItemMeta();
		meta1.setColor(Color.ORANGE);
		
		
		ItemStack pants = new ItemStack(Material.LEATHER_LEGGINGS, 1);
		LeatherArmorMeta meta2 = (LeatherArmorMeta)pants.getItemMeta();
		meta2.setColor(Color.GREEN);
		
		
		ItemStack boots = new ItemStack(Material.LEATHER_BOOTS);
		LeatherArmorMeta meta3 = (LeatherArmorMeta)boots.getItemMeta();
		meta3.setColor(Color.PURPLE);
		
		
		ItemStack sword = new ItemStack(Material.IRON_SWORD, 1);
		ItemMeta meta4 = sword.getItemMeta();
		
		ItemStack food = new ItemStack(Material.COOKED_BEEF, 64);
		ItemMeta meta5 = food.getItemMeta();
		
		
		if(commandLabel.equalsIgnoreCase("armorer"))
		{	
		if(args.length==0)
		{
		
		PlayerInventory pi = player.getInventory();
		pi.clear();
		pi.setHelmet(is);
        pi.setChestplate(is);
        pi.setLeggings(is);
        pi.setBoots(is);
		
		ItemStack achest = new ItemStack(Material.IRON_CHESTPLATE, 1);
		ItemMeta metaa = achest.getItemMeta();
		metaa.setDisplayName(ChatColor.DARK_PURPLE+"Armorer chestplate");
		achest.setItemMeta(metaa);
		
		
		meta4.setDisplayName(ChatColor.DARK_PURPLE+"Armorer sword");
		sword.setItemMeta(meta4);
		
		meta.setDisplayName(ChatColor.DARK_PURPLE+"Armorer helmet");
		helm.setItemMeta(meta);
		meta2.setDisplayName(ChatColor.DARK_PURPLE+"Armorer pants");
		pants.setItemMeta(meta2);
		meta3.setDisplayName(ChatColor.DARK_PURPLE+"Armorer boots");
		boots.setItemMeta(meta3);
		achest.addEnchantment(Enchantment.PROTECTION_ENVIRONMENTAL, 3);
		meta5.setDisplayName(ChatColor.DARK_PURPLE+"Armorer food");
		food.setItemMeta(meta5);
		helm.addUnsafeEnchantment(Enchantment.LUCK, 3);
		achest.addUnsafeEnchantment(Enchantment.LUCK, 3);
		pants.addUnsafeEnchantment(Enchantment.LUCK, 3);
		boots.addUnsafeEnchantment(Enchantment.LUCK, 3);
		 pi.setHelmet(helm);
		 pi.setChestplate(achest);
		 pi.setLeggings(pants);
		 pi.setBoots(boots);
		 pi.addItem(sword);
		 pi.addItem(food);
}
		}
		else if(commandLabel.equalsIgnoreCase("Archer"))
		{	
		if(args.length==0)
		{
			
			
			
		PlayerInventory pi = player.getInventory();
		
		pi.clear();
		pi.setHelmet(is);
        pi.setChestplate(is);
        pi.setLeggings(is);
        pi.setBoots(is);
		
		ItemStack asword = new ItemStack(Material.STONE_SWORD, 1);
		ItemMeta metar = asword.getItemMeta();
		
		ItemStack abow = new ItemStack(Material.BOW, 1);
		ItemMeta metabow = abow.getItemMeta();
		
		ItemStack arrow= new ItemStack(Material.ARROW, 64);
		ItemMeta metarrow=arrow.getItemMeta();
		
		
		
		metar.setDisplayName(ChatColor.DARK_PURPLE+"Archer sword");
		asword.setItemMeta(metar);
		meta.setDisplayName(ChatColor.DARK_PURPLE+"Archer helmet");
		helm.setItemMeta(meta);
		meta1.setDisplayName(ChatColor.DARK_PURPLE+"Archer chestplate");
		chest.setItemMeta(meta1);
		meta2.setDisplayName(ChatColor.DARK_PURPLE+"Archer pants");
		pants.setItemMeta(meta2);
		meta3.setDisplayName(ChatColor.DARK_PURPLE+"Archer boots");
		boots.setItemMeta(meta3);
		meta4.setDisplayName(ChatColor.DARK_PURPLE+"Archer sword");
		asword.setItemMeta(metar);
		meta5.setDisplayName(ChatColor.DARK_PURPLE+"Archer food");
		food.setItemMeta(meta5);
		metabow.setDisplayName(ChatColor.DARK_PURPLE+"Archer bow");
		abow.setItemMeta(metabow);
		metarrow.setDisplayName(ChatColor.DARK_PURPLE+"Archer arrows");
		arrow.setItemMeta(metarrow);
		abow.addEnchantment(Enchantment.ARROW_INFINITE, 1);
		abow.addEnchantment(Enchantment.ARROW_DAMAGE, 3);
		helm.addUnsafeEnchantment(Enchantment.LUCK, 3);
		chest.addUnsafeEnchantment(Enchantment.LUCK, 3);
		pants.addUnsafeEnchantment(Enchantment.LUCK, 3);
		boots.addUnsafeEnchantment(Enchantment.LUCK, 3); 
		pi.setHelmet(helm);
		 pi.setChestplate(chest);
		 pi.setLeggings(pants);
		 pi.setBoots(boots);
		 pi.addItem(asword);
		 pi.addItem(abow);
		 pi.addItem(food);
		 pi.addItem(arrow);
		
}
		
}
		return false;
	}
	
	
}
		  

