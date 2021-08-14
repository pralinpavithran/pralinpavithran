

#include <iostream>

using namespace std;

class storeKeeper
{
int itemcode,count;
string name, ManagerResp,MD;
    
    public:
    int add_product()
    {
        cout <<"enter Name, Item Code, Count of the product, Manager Responsible for the part, Maintenance Division";
        cin>>name>>itemcode>>count>>ManagerResp>>MD;
    }
    int delete_product()
    {
        
    }
    int update_count()
    {
        
    }
    void modify_product()
    {
        
    }
    void search_product()
    {
        cout<<"store keeper search";
    }
    
    
};
class Manager{
    


 public:
    void availability()
    {
        cout<<"availability";
    }
    void search_product()
    {
        cout<<"manager search";
    }

    void view()
    {
        cout<<"view";
    }

    
};
class MaintenanceEngineer: public Manager{
    public:
    void MaintainStock()
    {
        
    }
    

};

int main()
{
    int user,action,itemcode;
    storeKeeper st1;
    Manager Mg1;
    MaintenanceEngineer MN;
    

    
    
    cout<<"\t\tAircraft Parts Management\n\n";
    cout<<"1    Store Keeper\n";
    cout<<"2    Manager\n";
    cout<<"3    Maintenance Engineer\n\n";
    
    cout<<"select user\t";
    cin>>user;
    
    switch(user)
    {
        case 1: cout<<"StoreKeeper Options\n";
                cout<<"1 add_product\n";
                cout<<"2 delete_product\n";
                cout<<"3 update_count\n";
                cout<<"4 search_product\n";
                cout<<"Select action to perform";
                cin>>action;
                if(action==1)
                {
                    st1.add_product();
                    
                }
                else if(action ==2)
                {
                    st1.delete_product();
                    
                }
                else if (action ==3)
                {
                    st1.update_count();
                    
                }
                else if(action == 4)
                {
                    st1.search_product();
                }
                else
                cout<<"invalid action\n";
                break;
                
        case 2: cout<<"Manager\n\n";
                cout<< "1. search_product\n"  ;
                cout<< "2. view\n";
                cout<< "3. Availability\n";
                cout<<"select action to perform";
                cin>>action;
                if(action == 1)
                {
                    Mg1.search_product();
                }
                else if(action ==2)
                {
                    Mg1.view();
                }
                else if(action ==3)
                {
                    Mg1.availability();
                }
                else
                cout<<"invalid action\n";
                
                break;
         case 3: cout<<"Maintenance Engineer";
                 cout<<"enter item code to view product";
                 cin>>itemcode;
                 if(itemcode == 555)
                 {
                     MN.view();
                     cout<<"view product";
                 }
                 else
                 {
                     cout<<"no product found";
                 }
    }
    
 
           

    return 0;
}

    
