# AKGCheckListButton
`AKGCheckListButton ` is an easy to use and highly customizable radio buttons control for iOS. It's a subclass of `UIButton`, and works smoothly with`Swift`.


Make Object of AKGCheckListButtonModel like 
eg :

        let croissant = AKGCheckListButtonModel(lblText : "Croissant" ,identifire : "Croissant" ,selected : true)
        let eclair = AKGCheckListButtonModel(lblText : "Éclair" ,identifire : "Éclair" ,selected : false)
        let kouignAmann = AKGCheckListButtonModel(lblText : "Kouign amann" ,identifire : "Kouign amann" ,selected : false)
        let operacake = AKGCheckListButtonModel(lblText : "Opera cake" ,identifire : "Opera cake" ,selected : false)
        let macarons = AKGCheckListButtonModel(lblText : "Macarons" ,identifire : "Macarons" ,selected : false)
        let millefeuille = AKGCheckListButtonModel(lblText : "Mille-feuille" ,identifire : "Mille-feuille" ,selected : false)
        
        akgCheckListButtonModel = [croissant,eclair,kouignAmann,operacake,macarons,millefeuille]
        

Initialised AKGCheckListButtonGroupView object and pass parameter Group name ,AKGCheckListButtonModel array, and positions 

eg :

    let  akgRBGroupView = AKGCheckListButtonGroupView(akgCheckListButtonModel : akgCheckListButtonModel! ,akgCheckListButtonGroupName : "Order" , akgCheckListButtonGroupPosstion : size, selctionMode: SelctionMode.MultipleSelection)
        akgRBGroupView.setupView()
        akgRBGroupView.delegate = self
        self.view.addSubview(akgRBGroupView)

After selection Check List Button result will got in delegate 
eg :

 
     func selectedResult(resultObject:[AKGCheckListButtonModel]){
        print("Selected CheckList Button -> \(resultObject.count)")
     }
