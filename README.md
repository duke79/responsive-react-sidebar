Responsive React Sidebar  [![npm version](https://badge.fury.io/js/responsive-react-sidebar.svg)](http://badge.fury.io/js/react-sidebar)
=============

Responsive React Sidebar is a sidebar component for React with responsive design.

Installation
------------
`npm install responsive-react-sidebar`

Getting started
-----------------

```jsx
import React from 'react';
import ResponsiveSidebar from 'responsive-react-sidebar';

class App extends React.Component {
  onSideNavHidden() {
        //Probably switch the z-index of the rest of the page in case it's fixed
        //$("." + styles["Wrapper"]).css("z-index", "");
  }

  render() {
    return (
       <ResponsiveSidebar
            onScrimClick={this.onSideNavHidden.bind(this)}
            menu={
              header: {
                  "type": "item",
                  "value": "Vilokan Labs",
                  "link": "/"
                },
              container: [
                  {
                    "type": "item",
                    "value": "Project",
                    "link": "/project"
                  },
                  {
                    "type": "submenu",
                    "value": "Issues",
                    "link": "",
                    "items": [                    
                        {
                            "type": "subitem",
                            "value": "Service Desk",
                            "link": "/service_desk"
                        },
                        {
                            "type": "subitem",
                            "value": "Milestones",
                            "link": "/milestones"
                        }
                      ]
                  },
                  {
                      "type": "item",
                      "value": "Members",
                      "link": "/members"
                  },
                  {
                      "type": "item",
                      "value": "Wiki",
                      "link": "/wiki"
                  }            
              ],
              footer: {
                  "type": "item",
                  "value": "<< Collapse Sidebar",
                  "link": ""
              }
              } 
        />
    );
  }
}

export default App;
```