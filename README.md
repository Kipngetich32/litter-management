# Littter-Management-Software
class Registration:
    #registration of New shoppers using Pickle and a dictionary
    import pickle
    list1 ={}

    while True:
        def regi():
            global list1
            name= str (input("Enter New shopper:"))
            ID=str (input("Enter shoppers' ID:"))
            list1.update( {name:ID})
            
            
            output= open ('save.pkl','wb')

            pickle.dump (list1,output)
            output.close()

            inputFile= open('save.pkl','rb')

            list1=pickle.load(inputFile)
            inputFile.close()

            print ("List of shoppers :"+str(list1))
            Exit =input ("Press Enter to continue or Q to exit :")
            if Exit== "Q":
            print ("First part ok")
            
class MENU(Registration):
    def Menu():
            print ("To Register enter 1")
            print ("To ADD Shopper enter 2")
            print ("To Add Litter enter 3")
            print ("To exit enter Q")
            Choice = input(str ("Enter:"))
            print (Choice)
            if Choice == "1": 
                    Registration.Regi()
            elif Choice=="2":
                    print ("shopper")
            elif Choice=="3":
                    print ("litter")
            elif Choice=="Q":
                    print ("exit")
            else :
                raise ValueError ("Inavalid Choice")
call= MENU()
call.Menu()


   
