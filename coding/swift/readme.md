
SOP-0-init-var-let


Objectives

减少编程的随意性(arbitrariness) and/or ambiguity


Lazy var vs let


If let, with = {}(), then in closure you cannot refer to any self-related methods, etc.

Otherwise, you will occur errors looking like this:

` Value of type 'NSObject -> () -> YourClass' has no member 'yourMethod'`


If lazy var , you can.

If possible, it is encouraged to bring standalone property building code into let or lazy-var constructs, rather than in init().


Purpose of properties.



Let is safer (with more focus scope and lifecycle) than var. which may not be re-assigned other than initial time.

Private properties are safer than public ones.


# SOP-0-MethodAttributes


## Classification

Classification | Features | Impl. Notes
--|--|--
Main func. Interface | | open or public
Assist func – branch/condition (width) | For different cases | Private or internal . subclassable ?  <br/> Interface (params and returns) are similar to main <br/> Params may be subclass of main’s , or conforming to protocol as main’s param
Assist func – to break down. / drill down (depth) | Interface (params and returns) are different from main |
Alternative solution | Not in used.
Callback
Internal – helper /service



Condition

Functional
Guard all necessary conditions, otherwise return or fatalError?


## Who defines/declares the method


Definer | Examples
--|--
iOS Framework defined | func viewDidLoad()
iOS Framework defined in protocol: // UISearchBarDelegate |  func searchBar(searchBar: UISearchBar, textDidChange searchText: String)
role specific methods.  <br>Note: role (such as UIVC) is greater than base class (such as UIViewController) |Such as \_styling(), in UIVC.
@IBAction |@IBAction func action_close(sender: AnyObject)  <br/>should translate into semantics. And call model/logic specific func.


# SOP-0-PropertyAttributes


Purpose


Purpose | Swift
Input | Optional , var
Output | Optional , var
Service |private, Let or lazy var, non-optional | Created up front.

## For input and output of a func,  Property vs vs func’s paras and return

If params and return are many.

Not support Async call



Property vs func’s paras and return


func’s paras and return, cons

    @IBOutlet weak var labelGreeting: UILabel!




Refs

Swift PG (2.2) / Properties
