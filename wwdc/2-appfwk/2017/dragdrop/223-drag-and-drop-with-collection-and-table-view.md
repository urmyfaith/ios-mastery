
# [223 Drag and Drop with Collection and Table View](https://developer.apple.com/videos/play/wwdc2017/223/)


* Tyler Fox, UIKit Engineer
* Mohammed Jisrawi, iOS Engineer
* Steve Breen, UIKit Engineer


Drag and Drop API
Collection and Table View
Focused around cells and index paths Fluid animations
Asynchronous data loading Consistent API for both


Agenda

* Basics
* Perfecting drops
* Final touches

## Basics

### Beginning a Drag

One required method on dragDelegate
```

func collectionView(_: UICollectionView,  itemsForBeginning: UIDragSession,
at: IndexPath) -> [UIDragItem]

```
Return an empty array to prevent the drag

### Adding Items to a Drag Session

Opt-in via optional method on dragDelegate
`func collectionView(_: UICollectionView,  itemsForAddingTo: UIDragSession,
at: IndexPath,
point: CGPoint) -> [UIDragItem]`

Return an empty array to handle the tap normally

### Accepting a Drop

One required method on dropDelegate

Drop coordinator

* Access dropped items
* Update collection/table view
* Specify animations


## Demo


## Drop Animation


## Introducing Placeholders (28)


### the Placeholder Context


## Demo Placeholder


## Final touches


### Reordering


### Spring loading

## Customizing Cell Appearance

.none .lifting .dragging

### Customizing the Drag Preview


### Next Steps

[`UISpringLoadedInteractionSupporting`](https://developer.apple.com/documentation/uikit/uispringloadedinteractionsupporting)

[`UISpringLoadedInteraction`](https://developer.apple.com/documentation/uikit/uispringloadedinteraction)

## API

x | [Table View](https://developer.apple.com/documentation/uikit/views_and_controls/table_views) | [Collection Views](https://developer.apple.com/documentation/uikit/views_and_controls/collection_views)
guide | [Supporting Drag and Drop in Table Views](https://developer.apple.com/documentation/uikit/views_and_controls/table_views/supporting_drag_and_drop_in_table_views)
x | [`UITableViewDragDelegate`](https://developer.apple.com/documentation/uikit/uitableviewdragdelegate) | [`UICollectionViewDragDelegate`](https://developer.apple.com/documentation/uikit/uicollectionviewdragdelegate)
x | [`UITableViewDropDelegate`](https://developer.apple.com/documentation/uikit/uitableviewdropdelegate) | [`UICollectionViewDropDelegate`](https://developer.apple.com/documentation/uikit/uicollectionviewdropdelegate)
x | [`UITableViewDropCoordinator`](https://developer.apple.com/documentation/uikit/uitableviewdropcoordinator) | [`UICollectionViewDropCoordinator`](https://developer.apple.com/documentation/uikit/uicollectionviewdropcoordinator)
class | [`UITableViewDropProposal`](https://developer.apple.com/documentation/uikit/uitableviewdropproposal)
protocol | [`UITableViewDropItem`](https://developer.apple.com/documentation/uikit/uitableviewdropitem)
protocol | [`UITableViewDropPlaceholderContext`](https://developer.apple.com/documentation/uikit/uitableviewdropplaceholdercontext)


[`UIDataSourceTranslating`](https://developer.apple.com/documentation/uikit/uidatasourcetranslating)
