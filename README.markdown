# DDBadgeViewCell for UITableView

DDBadgeViewCell is a UITableViewCell subclass that has a customizable badge view on the right. With fast Quartz 2D path drawing and blending, one can use this with very large data set and still keep great performance when scrolling.

![](https://github.com/digdog/DDBadgeViewCell/raw/master/screenshot.png)
![](https://github.com/bdunagan/DDBadgeViewCell/raw/master/screenshot2.png)

## Requirement

1. iPhone SDK 3.1 or later (Sample project was created in iPhone SDK 4).
2. QuartzCore.framework should be included in your project.

## Usage

Like regular UITableViewCell, you create them in - (UITableViewCell *)tableView:cellForRowAtIndexPath:

    DDBadgeViewCell *cell = (DDBadgeViewCell *)[tableView dequeueReusableCellWithIdentifier:CellIdentifier];
    if (cell == nil) {
        cell = [[[DDBadgeViewCell alloc] initWithStyle:UITableViewCellStyleDefault reuseIdentifier:CellIdentifier] autorelease];
    }
    
And configure the cell through its properties below:

	cell.summary = @"Summary";
	cell.detail = @"Detail text goes here";
	cell.badgeText = @"Badge Text";
	cell.badgeColor = [UIColor orangeColor];
	cell.badgeHighlightedColor = [UIColor lightGrayColor];
	
## License

DDBadgeViewCell is released under MIT License.
