# $NetBSD: Makefile,v 1.14 2017/11/23 17:20:21 wiz Exp $

DISTNAME=	xfce4-whiskermenu-plugin-2.1.2
PKGREVISION=	1
CATEGORIES=	x11
MASTER_SITES=	http://archive.xfce.org/src/panel-plugins/xfce4-whiskermenu-plugin/2.1/

EXTRACT_SUFX=	.tar.bz2
LICENSE=	gnu-gpl-v2

MAINTAINER=	youri@NetBSD.org
HOMEPAGE=	https://gottcode.org/xfce4-whiskermenu-plugin/
COMMENT=	Alternate application launcher for Xfce

USE_CMAKE=	yes
USE_LANGUAGES=	c c++
USE_TOOLS+=	gmake pkg-config msgfmt perl intltool

.include "../../x11/xfce4-garcon/buildlink3.mk"
.include "../../x11/xfce4-panel/buildlink3.mk"
.include "../../x11/xfce4-exo/buildlink3.mk"
.include "../../graphics/hicolor-icon-theme/buildlink3.mk"
.include "../../mk/bsd.pkg.mk"
